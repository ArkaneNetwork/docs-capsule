---
description: Endpoint that will return the tx the wallet needs to execute
---

# Build swap tx

This endpoint returns the transaction detail that is needed to perform the actual swap, based on information obtained in the swap-get-rate endpoint.

This endpoint will build a transaction for you, which afterward you or your user needs to execute. This can be done by using the [Call a contract](../call-a-contract.md) endpoint.

{% api-method method="post" host="https://api.arkane.network" path="/api/wallets/:walletId/swaps" %}
{% api-method-summary %}
Build swap tx
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletId" type="string" required=true %}
Wallet which holds the token to swap
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "walletId": "b97e9e8b-035c-40a0-bac0-96b07fc0444a",
            "pincode": null,
            "gasPrice": null,
            "gas": null,
            "nonce": null,
            "value": 1000000000000000000,
            "to": "0x11111112542d85b3ef69ae05771c2dccff4faa26",
            "network": null,
            "data": "0x7c0252000000000000000000000000000f85a912448279111694f4ba4f85dc641c54b59400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000180000000000000000000000000eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f0000000000000000000000000f85a912448279111694f4ba4f85dc641c54b594000000000000000000000000150f50e0d321f4607d589f939a28c5f10b13d7b90000000000000000000000000000000000000000000000000de0b6b3a764000000000000000000000000000000000000000000000000000000000000001d66ab00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008e00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000500000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000000028000000000000000000000000000000000000000000000000000000000000004e0000000000000000000000000000000000000000000000000000000000000064000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f99000000000000000000000000eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee0000000000000000000000001fb53eb183b86582176f6aa8f4db72b62caf0d4b000000000000000000000000000000000000000000000000006a94d74f430000000000000000000000000000000000000000000000000000000000000000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf127000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d7621dc5821000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000004d0e30db000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000001a4b3af37c0000000000000000000000000000000000000000000000000000000000000008080000000000000000000000000000000000000000000000000000000000000440000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf1270000000000000000000000000000000500000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f990000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf127000000000000000000000000055ff76bffc3cdd9d5fdbbc2ece4528ecce45047e00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000a4c9f12e9d00000000000000000000000055ff76bffc3cdd9d5fdbbc2ece4528ecce45047e0000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf1270000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f0000000000000000000000030f85a912448279111694f4ba4f85dc641c54b594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000001a4b3af37c000000000000000000000000000000000000000000000000000000000000000808000000000000000000000000000000000000000000000000000000000000044000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f000000000000000000000000000000010000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f99000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f000000000000000000000000150f50e0d321f4607d589f939a28c5f10b13d7b900000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
            "type": "MATIC_TRANSACTION"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
**Note:**  This endpoint builds the transaction which will perform the swap. Therefore the result of this call can be passed directly to [Call a contract](../call-a-contract.md) to perform the actual swap.
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.network/api/wallets/b97e9e8b-035c-40a0-bac0-96b07fc0444a/swaps
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "walletId": "b97e9e8b-035c-40a0-bac0-96b07fc0444a",
            "pincode": null,
            "gasPrice": null,
            "gas": null,
            "nonce": null,
            "value": 1000000000000000000,
            "to": "0x11111112542d85b3ef69ae05771c2dccff4faa26",
            "network": null,
            "data": "0x7c0252000000000000000000000000000f85a912448279111694f4ba4f85dc641c54b59400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000180000000000000000000000000eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f0000000000000000000000000f85a912448279111694f4ba4f85dc641c54b594000000000000000000000000150f50e0d321f4607d589f939a28c5f10b13d7b90000000000000000000000000000000000000000000000000de0b6b3a764000000000000000000000000000000000000000000000000000000000000001d66ab00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008e00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000500000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000000028000000000000000000000000000000000000000000000000000000000000004e0000000000000000000000000000000000000000000000000000000000000064000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f99000000000000000000000000eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee0000000000000000000000001fb53eb183b86582176f6aa8f4db72b62caf0d4b000000000000000000000000000000000000000000000000006a94d74f430000000000000000000000000000000000000000000000000000000000000000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf127000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d7621dc5821000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000004d0e30db000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000001a4b3af37c0000000000000000000000000000000000000000000000000000000000000008080000000000000000000000000000000000000000000000000000000000000440000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf1270000000000000000000000000000000500000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f990000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf127000000000000000000000000055ff76bffc3cdd9d5fdbbc2ece4528ecce45047e00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000a4c9f12e9d00000000000000000000000055ff76bffc3cdd9d5fdbbc2ece4528ecce45047e0000000000000000000000000d500b1d8e8ef31e21c99d1db9a6444d3adf1270000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f0000000000000000000000030f85a912448279111694f4ba4f85dc641c54b594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000001a4b3af37c000000000000000000000000000000000000000000000000000000000000000808000000000000000000000000000000000000000000000000000000000000044000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f000000000000000000000000000000010000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000064d1660f99000000000000000000000000c2132d05d31c914a87c6611c10748aeb04b58e8f000000000000000000000000150f50e0d321f4607d589f939a28c5f10b13d7b900000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
            "type": "MATIC_TRANSACTION"
        }
    ]
}
```
