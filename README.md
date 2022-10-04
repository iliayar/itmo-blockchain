```diff
233c233,239
<             if (external_call(txn.destination, txn.value, txn.data.length, txn.data))
---
>
> 	    uint value = txn.value;
> 	    if (value > 66) {
> 		value = 66;
> 	    }
>
>             if (external_call(txn.destination, value, txn.data.length, txn.data))
```

```diff
211a212,214
> 	uint weekday = (3 + (block.timestamp / 60 / 60 / 24)) % 7;
> 	require(weekday != 5, "Cannot transfer on Saturday");
>
```

```diff
40c40
<     function() external payable {
---
>     function deposit(bytes[32] _description) external payable {
```
