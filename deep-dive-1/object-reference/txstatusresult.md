# TxStatusResult

## Signature

```javascript
{
    status: 'UNKNOWN' | 'PENDING' | 'FAILED' | 'SUCCEEDED'
}
```

## Parameters

| Parameter | Type     | Description                                                                                                                                                                                                                               |
| --------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `status`  | `String` | <ul><li><code>UNKNOWN</code> Not yet visible on the chain.</li><li><code>PENDING</code> Not yet completed (or failed).</li><li><code>SUCCEEDED</code> Completed successfully</li><li><code>FAILED</code> Transaction is failed.</li></ul> |

## Example

```javascript
{
  "secretType" : "ETHEREUM",
  "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
  "data" : "I agree with terms and conditions"
}
```
