---
description: >-
  How to perform a basic token transfer. E.g transfer ETH from one wallet to
  another.
---

# Transfer a native token

{% api-method method="post" host="https://api.arkane.network" path="/api/transactions/execute" %}
{% api-method-summary %}
Transfer a native token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="pincode" type="string" required=true %}
PIN related to the wallet ID
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
TRANSFER
{% endapi-method-parameter %}

{% api-method-parameter name="walletId" type="string" required=true %}
The id of the wallet that will initiate the tx
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

```javascript
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
🧙 The destination of a transfer is not limited to a blockchain address, we also support **email addresses**.
{% endhint %}

## Example 

#### Request 

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

{% page-ref page="../../deep-dive-1/object-reference/transferrequestdto.md" %}



