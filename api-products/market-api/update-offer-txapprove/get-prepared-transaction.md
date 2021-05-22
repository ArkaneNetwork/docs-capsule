---
description: >-
  Endpoint that returns the specific Approve transction an end-user needs to
  launch
---

# Get prepared Approve tx

Since there are multiple variants and standards of NFT contracts it can be difficult for a client to know for each NFT contract which function to call and which input parameter each function might need. To overcome that specific pain the market also provides an endpoint that returns that required information, allowing the client to easily query what they need to forward to their end-users. 

{% api-method method="get" host="https://api.arkane.market" path="/offers/:offerId/preparation/transactions" %}
{% api-method-summary %}
Get prepared Approve transaction
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="offerId" type="string" required=true %}
ID of the offer
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "type": "CONTRACT_EXECUTION",
            "to": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
            "secretType": "MATIC",
            "value": 0,
            "functionName": "setApprovalForAll",
            "inputs": [
                {
                    "type": "address",
                    "value": "0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888"
                },
                {
                    "type": "bool",
                    "value": "true"
                }
            ],
            "data": "0xa22cb465000000000000000000000000e885a1cd1b67bdc352a113ab2e6a5fc6c924f8880000000000000000000000000000000000000000000000000000000000000001"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
**Note**: When the end-user has executed the result of this call, that transaction hash should be providing back to the market by using [Update offer: TxApprove](./).
{% endhint %}

## What if the result set is empty?

It is possible that in certain cases the call was successful, but that the result set is empty. This means that the wallet that stores the NFT, approved the market in the past for that specific NFT contract. Therefore the end-user is not required to perform the Approve transaction for a second time. In this case the [Update offer: TxApprove](./) step can be skipped and moved directly to [Update offer: Signature](../update-offer-signature.md).

```javascript
{
    "success": true,
    "result": []
}
```

## Example

#### Request

```javascript
https://api.arkane.market/offers/b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5/preparation/transactions
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "type": "CONTRACT_EXECUTION",
            "to": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
            "secretType": "MATIC",
            "value": 0,
            "functionName": "setApprovalForAll",
            "inputs": [
                {
                    "type": "address",
                    "value": "0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888"
                },
                {
                    "type": "bool",
                    "value": "true"
                }
            ],
            "data": "0xa22cb465000000000000000000000000e885a1cd1b67bdc352a113ab2e6a5fc6c924f8880000000000000000000000000000000000000000000000000000000000000001"
        }
    ]
}
```

