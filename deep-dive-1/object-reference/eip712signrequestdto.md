# Eip712SignRequestDto

## Signature

```javascript
{
  secretType! : SecretType,
  walletId! : string,
  data! : any
}
```

## Parameters

| Parameter    | Required | Type                                                                    | Description                                       |
| ------------ | -------- | ----------------------------------------------------------------------- | ------------------------------------------------- |
| `walletId`   | `True`   | `String`                                                                | ID of the wallet one wants to sign with.          |
| `secretType` | `True`   | [`SecretType`](broken-reference)                                        | Chain the transaction will be executed on.        |
| `data`       | `True`   | <p><code>JSON</code></p><p><code>String(containing the JSON)</code></p> | Should contain valid JSON (keys should be quoted) |

## Example

```javascript
{
  "secretType" : "ETHEREUM",
  "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
  "data" : {
      "types":{
        "EIP712Domain":[
          {
            "name":"name",
            "type":"string"
          },
          {
            "name":"version",
            "type":"string"
          },
          {
            "name":"chainId",
            "type":"uint256"
          },
          {
            "name":"verifyingContract",
            "type":"address"
          },
          {
            "name":"salt",
            "type":"bytes32"
          }
        ],
        "Bid":[
          {
            "name":"amount",
            "type":"uint256"
          },
          {
            "name":"bidder",
            "type":"Identity"
          }
        ],
        "Identity":[
          {
            "name":"userId",
            "type":"uint256"
          },
          {
            "name":"wallet",
            "type":"address"
          }
        ]
      },
      "domain":{
        "name":"My amazing dApp",
        "version":"2",
        "chainId":1,
        "verifyingContract":"0x1C56346CD2A2Bf3202F771f50d3D14a367B48070",
        "salt":"0xf2d857f4a3edcb9b78b4d503bfe733db1e3f6cdc2b7971ee739626c97e86a558"
      },
      "primaryType":"Bid",
      "message":{
        "amount":100,
        "bidder":{
          "userId":323,
          "wallet":"0x3333333333333333333333333333333333333333"
        }
      }
    }
}
```
