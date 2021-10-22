---
description: >-
  How to perform a fungible transfer. E.g transfer an ERC20 token from one
  wallet to another.
---

# Transfer a fungible token

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/execute" method="post" summary="Transfer a fungible token" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="tokenAddress" type="string" %}
Token contract address
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN related to the wallet ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
TOKEN_TRANSFER
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" type="string" %}
Id of the wallet that will initiate the tx
{% endswagger-parameter %}

{% swagger-parameter in="body" name="to" type="string" %}
Destination Address (can be a blockchain address or email address)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="secretType" type="string" %}
On which blockchain the tx will be executed
{% endswagger-parameter %}

{% swagger-parameter in="body" name="value" type="integer" %}
Amount you want to transfer
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactionRequest" type="object" %}
transactionRequest object
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "success": true,
    "result": {
        "transactionHash": "0x8c953e09d8cede9f4eb0d1ee96de4f5a99e31dba7e64312bb252a465de12d10d"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
🧙 The destination of a token transfer is not limited to a blockchain address, we also support **email addresses**.
{% endhint %}

## Example&#x20;

#### Request&#x20;

```javascript
POST : https://api.arkane.network/api/transactions/execute
```

#### Request Body

```javascript
{
  "transactionRequest" : {
    "type" : "TOKEN_TRANSFER",
    "walletId" : "edc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
    "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
    "secretType" : "MATIC",
    "tokenAddress" : "0x4df47b4969b2911c966506e3592c41389493953b",
    "value" : 1.15,
    "tokenId" : null
  }
  "pincode" : "1234",
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
