---
description: Small guide on how to burn an NFT
---

# How to burn an NFT

{% hint style="warning" %}
This guide assumes that the NFT that is going to be burned was created by our [NFT API](../../api-products/nft-api/) and therefore uses functions that are available in our contracts.
{% endhint %}

In order to burn an NFT, we will need to [execute a function](../../api-products/wallet-api/execute-contract-call.md) on the NFT contract. In the example below we are calling the contract `0xe80f3baa739c18fd4ebf97716529a4b85be464dd` and more specifically the function `burn`.&#x20;

As input parameters we have&#x20;

* Token id  (Token id that will get burned)
* Contract address  (Address of the contract that is managing the token)
* Amount  (Number of tokens to be burned, in case of an ERC1155 token)

![](<../../.gitbook/assets/image (26).png>)

**Endpoint**

```
POST: https://api.arkane.network/api/transactions/execute
```

**Request Body**

```json
{
    "pincode": "1234",
    "transactionRequest": {
        "type": "CONTRACT_EXECUTION",
        "walletId": "7a9a754e-6331-46a7-a5ac-e74b04df18d0",
        "to": "0xe80f3baa739c18fd4ebf97716529a4b85be464dd",
        "secretType": "MATIC",
        "functionName": "burn",
        "inputs": [
            {
                "type": "uint256",
                "value": "402"
            },
            {
                "type": "address",
                "value": "0xe80f3baa739c18fd4ebf97716529a4b85be464dd"
            },
            {
                "type": "uint256",
                "value": "1"
            }
        ]
    }
}
```

### Burning multiple tokens

Our contract also allows you to burn multiple tokens with one transaction. For we use the `burnBatch` function instead of the `burn` function. The burnBatch function used Arrays as an input parameter for `id` and `amount`.&#x20;

![](<../../.gitbook/assets/image (27).png>)
