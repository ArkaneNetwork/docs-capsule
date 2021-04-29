---
description: Data structure for performing a non-fungible token transfer
---

# NftTransferRequestDto

## Signature

```javascript
{
  walletId! : string;
  to! : string;
  secretType! : SecretType;
  tokenAddress!: string;
  tokenId!: number;
    data? : string;
  value! : BigDecimal;
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet one wants to sign with. |
| `to` | `True` | `String` | Destination address of the transaction. Can be an address or an email address. |
| `secretType` | `True` | [`SecretType`](secrettype.md) | Chain the transaction will be executed on. |
| `tokenAddress` | `True` | `String` | Address of the token |
| `tokenId` | `True` | `Number` | ID of the non-fungible token or ERC20 token inside ERC1155 |
| `data` | `False` | `String` | Data you want to send. This field will be ignored when building a token transaction request |
| `value` | `True` | `Number` | Token value that should be transferred. |

## Example

```javascript
{
  "walletId" : "adc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "VECHAIN",
  "tokenAddress" : "0x4df47b4969b2911c966506e3592c41389493953b",
  "from" : "0x89e01cEC55D718fA1Bf6B00fF21e6707cd9A3067",
  "tokenId" : 1
}
```

## Function Reference

{% page-ref page="../../custody-wallets/wallet-api/transfer-a-non-fungible-token.md" %}



