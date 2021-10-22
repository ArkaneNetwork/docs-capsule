---
description: >-
  How to perform a basic token transfer. E.g transfer ETH from one wallet to
  another.
---

# Transfer a native token

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/execute" method="post" summary="Transfer a native token" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN related to the wallet ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
TRANSFER
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" type="string" %}
The id of the wallet that will initiate the tx
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
🧙 The destination of a transfer is not limited to a blockchain address, we also support **email addresses**.
{% endhint %}

## Example&#x20;

#### Request&#x20;

```javascript
POST : https://api.arkane.network/api/transactions/execute
```

#### Request Body

```javascript
{
   "transactionRequest": {
     "type": "TRANSFER",
     "walletId": "944124ed-305d-4e56-a0fd-bce1c7f1537c",
     "to": "0xf56799d7C95C6DEb708A9f55b2e75A685A94F980",
     "secretType": "ETHEREUM",
     "value": 0,
     "data": '' //optional
   },
   "pincode": "1234"
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

{% content-ref url="../../deep-dive-1/object-reference/transferrequestdto.md" %}
[transferrequestdto.md](../../deep-dive-1/object-reference/transferrequestdto.md)
{% endcontent-ref %}

