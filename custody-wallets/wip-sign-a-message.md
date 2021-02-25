---
description: Signs arbitrary data using a specific wallet.
---

# Sign a message

{% api-method method="post" host="https://api.arkane.network" path="/api/signatures" %}
{% api-method-summary %}
Transfer a non-fungible token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="signatureRequest" type="object" required=true %}
Contains the signature request
{% endapi-method-parameter %}

{% api-method-parameter name="signatureRequest.type" type="string" required=true %}
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

```

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
POST : https://api.arkane.network/api/signatures
```

#### Request Body

```javascript
{
    "pincode" : "1234",
    "signatureRequest" : 
    {
        "type" : "MESSAGE",
        "secretType" : "ETHEREUM",
        "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
        "data" : "I agree with terms and conditions"
    }
}
```

#### Response

```javascript
{
  "type" : "HEX_SIGNATURE",
  "r" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd",
  "s" : "0x6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a029",
  "v" : "0x1c",
  "signature" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a0291c"
}
```

