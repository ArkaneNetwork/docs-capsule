---
description: >-
  How to perform a non-fungible transfer. E.g transfer an ERC721 or ERC1155
  token from one wallet to another.
---

# Transfer a non-fungible token

{% api-method method="post" host="https://api.arkane.network" path="/api/transactions/execute" %}
{% api-method-summary %}
Transfer a non-fungible token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="tokenId" type="string" required=true %}
NFT Token ID
{% endapi-method-parameter %}

{% api-method-parameter name="tokenAddress" type="string" required=true %}
NFT Token contract address
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
PIN related to the wallet ID
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
NFT\_TRANSFER
{% endapi-method-parameter %}

{% api-method-parameter name="walletId" type="string" required=true %}
Id of the wallet that will initiate the tx
{% endapi-method-parameter %}

{% api-method-parameter name="to" type="string" required=true %}
Destination Address \(can be a blockchain address or email address\)
{% endapi-method-parameter %}

{% api-method-parameter name="secretType" type="string" required=true %}
On which blockchain the tx will be executed
{% endapi-method-parameter %}

{% api-method-parameter name="value" type="integer" required=true %}
Amount you want to transfer
{% endapi-method-parameter %}

{% api-method-parameter name="transactionRequest" type="object" required=true %}
transactionRequest object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```java
{
    "success": true,
    "result": {
        "transactionHash": "0x8c953e09d8cede9f4eb0d1ee96de4f5a99e31dba7e64312bb252a465de12d10d"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
🧙 The destination of a token transfer is not limited to a blockchain address, we also support **email addresses**.
{% endhint %}

## Example 

#### Request 

```javascript
POST : https://api.arkane.network/api/transactions/execute
```

#### Request Body

```javascript
{
  "transactionRequest" : {
    "type" : "NFT_TRANSFER",
    "walletId" : "adc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
    "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
    "secretType" : "MATIC",
    "tokenAddress" : "0x4df47b4969b2911c966506e3592c41389493953b",
    "tokenId" : 1
  }
  "pincode" : "1234"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "transactionHash": "0x8c953e09d8cede9f4eb0d1ee96de4f5a99e31dba7e64312bb252a465de12d10d"
    }
}
```

