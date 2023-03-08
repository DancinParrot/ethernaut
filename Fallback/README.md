# Fallback

View contributions
```Solidity
await contract.contributions('0x9CB391dbcD447E645D6Cb55dE6ca23164130D008').then(v => v.toString())
```

Send Transaction using the contract's ABI
```Solidity
await contract.contribute.sendTransaction({ from: player, value: toWei('0.0009')})
// the contract requires eth < 0.001, hence we use a value of 0.0009 then convert 
// to WEI

await contract.contribute(any args, { value: toWei('0.0009') })
```

Send transaction to trigger the receive() fallback function
```Solidity
await sendTransaction({from: player, to: contract.address, value: toWei('0.000001')})
```
