---
description: Data structure for performing a native token transfer
---

# TransferRequestDto

## Signature

```javascript
{
  walletId! : string;
  to! : string;
  secretType! : SecretType;
  data! : string;
  value! : BigDecimal;
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet one wants to sign with. |
| `to` | `True` | `String` | Destination address of the transaction. Can be an address or an email address. |
| `secretType` | `True` | [`SecretType`]() | Chain the transaction will be executed on. |
| `data` | `False` | `String` | Data you want to send. This field will be ignored when building a token transaction request |
| `value` | `True` | `Number` | Token value that should be transferred. |

{% hint style="info" %}
🧙 You don’t have to take into account the number of decimals for different tokens, Arkane handles that for you.

**Example:** If a token has 18 decimals and you want to transfer 1 token, provide the value 1. Arkane will translate this to the correct nondecimal value \(1 \* 10e18\).
{% endhint %}

## Example

```javascript
{
  "walletId" : "cdc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "VECHAIN",
   "data" : "0x",
  "value" : 1.15
}
```

## Function Reference

{% page-ref page="../../custody-wallets/transfer-a-native-token.md" %}

