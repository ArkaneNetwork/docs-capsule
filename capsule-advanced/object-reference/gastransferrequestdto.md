---
description: Data structure for performing a gas transfer
---

# GasTransferRequestDto

## Signature

```javascript
{
  walletId! : string;
  to! : string;
  secretType! : SecretType;
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
| `data` | `False` | `String` | Data you want to send. This field will be ignored when building a token transaction request |
| `value` | `True` | `Number` | Token value that should be transferred. |

{% hint style="info" %}
🧙 You don’t have to take into account the number of decimals for different tokens, Arkane handles that for you.

**Example:** If a token has 18 decimals and you want to transfer 1 token, provide the value 1. Arkane will translate this to the correct nondecimal value \(1 \* 10e18\).
{% endhint %}

## Example

```javascript
{
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 81,
    secretType: 'ETHEREUM',
}
```

## Function Reference

{% page-ref page="../../custody-wallets/transfer-a-native-token.md" %}

