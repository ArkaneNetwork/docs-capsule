---
description: Object that contains all the items for a wallet
---

# WalletItems

## Signature

```javascript
{
    walletId: string;
    walletAddress: string;
    secretType: SecretType;
    items: NFT[];
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet |
| `walletAddress` | `True` | `String` | The blockchain address of the wallet |
| `items` | `True` | [`NFT[]`](nft.md) | A list of NFT's for this wallet |

