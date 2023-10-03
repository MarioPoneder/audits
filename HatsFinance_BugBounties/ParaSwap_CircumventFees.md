**Description**\
The following is true for any swap/buy method of the [SimpleSwap](https://etherscan.io/address/0x66C1c25d7D2bd4A32Ed33501E202B275030f402C#code)/[MultiPath](https://etherscan.io/address/0xbD7b550d2E7571383d84ACF597a00d341E5C406E#code) contracts which are delegatecalled by the [AugustusSwapper](https://etherscan.io/address/0xDEF171Fe48CF0115B1d80b88dc8eAB59176FEe57), i.e. `simpleBuy/simpleSwap/buy/multiSwap/megaSwap`.  
Calling any of those methods with `data.partner = address(0)` leads to `_getFixedFeeBps(data.partner, data.feePercent) == 0` which already circumvents fee payments at many intances of the mentioned contracts, see the follwing code snippet from `SimpleSwap.performSimpleSwap(...)`:
```solidity
        if (
            _getFixedFeeBps(partner, feePercent) != 0 && !_isTakeFeeFromSrcToken(feePercent) && !_isReferral(feePercent)
        ) {
            // take fee from dest token
            takeToTokenFeeAndTransfer(toToken, receivedAmount, beneficiary, partner, feePercent);
        } else if (receivedAmount > expectedAmount && !_isTakeFeeFromSrcToken(feePercent)) {
            takeSlippageAndTransferSell(toToken, beneficiary, partner, receivedAmount, expectedAmount, feePercent);
        } else {
            // Transfer toToken to beneficiary
            Utils.transferTokens(toToken, beneficiary, receivedAmount);

            if (_getFixedFeeBps(partner, feePercent) != 0 && _isTakeFeeFromSrcToken(feePercent)) {
                // take fee from source token
                takeFromTokenFee(fromToken, fromAmount, partner, feePercent);
            }
        }
```
However, even when setting `data.partner = address(0)`, unallocated fees are still paid in some instances.  Therefore, one also has to set `data.expectedAmount` such that `receivedAmount > expectedAmount` or `amountIn < expectedAmount` or `fromAmount.sub(remainingAmount) < expectedAmount` (depeding on the actual usage in the code) always evaluates to `false`. This can be easily achieved by setting `data.expectedAmount` to `0` or `type(uint256).max` depending on the case, i.e. buy or swap. Moreover, this is possible without side effects, since `data.expectedAmount` is **never** used for slippage protection but only for fee computation.  

As a consequence, users can use the methods of SimpleSwap/MultiPath **in any case** without paying fees. Considering the accumulated amounts, despite regular withdrawals, in the [FeeClaimer](https://etherscan.io/address/0xeF13101C5bbD737cFb2bF00Bbd38c626AD6952F7) contract, this vulnerability leads to a huge loss of income for the protocol.

**Attack Scenario**\
On any call to `simpleBuy/simpleSwap/buy/multiSwap/megaSwap`:
1.  Set `data.partner = address(0)`
2.  Set `data.expectedAmount = type(uint256).max` on swaps or `data.expectedAmount = 0` on buys

**Proof of Concept**  
I am willing to provide the whole PoC project upon request.  


**Recommendation**
1. Do not allow `data.partner == address(0)`, this would also solve the problem of unallocated fees which can be stolen, see [other bug report](./ParaSwap_TheftOfFees.md).
2.  Revert on unrealistic deviation of `data.expectedAmount` from `data.toAmount` or additionally use `data.expectedAmount` for slippage protection in order to enforce realistic values.