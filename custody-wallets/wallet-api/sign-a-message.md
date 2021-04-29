---
description: Signs arbitrary data using a specific wallet.
---

# Sign a message

{% api-method method="post" host="https://api.arkane.network" path="/api/signatures" %}
{% api-method-summary %}
Sign a message
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="signatureRequest" type="object" required=true %}
Contains the signature request
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Signature type. \(MESSAGE or EIP712\)
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="string" required=true %}
The data to sign
{% endapi-method-parameter %}

{% api-method-parameter name="walletId" type="string" required=true %}
Id of the wallet that will initiate the tx
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
PIN related to the wallet ID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```java
{
  "type" : "HEX_SIGNATURE",
  "r" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd",
  "s" : "0x6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a029",
  "v" : "0x1c",
  "signature" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a0291c"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
🧙 The signatures endpoint supports the [EIP-712](https://eips.ethereum.org/EIPS/eip-712) standard, Ethereum typed structured data hashing and signing. This EIP aims to improve the usability of off-chain message signing for use on-chain.
{% endhint %}

## Example 

#### Request 

```javascript
POST : https://api.arkane.network/api/signatures
```

#### Request Body

```java
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

```java
{
  "type" : "HEX_SIGNATURE",
  "r" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd",
  "s" : "0x6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a029",
  "v" : "0x1c",
  "signature" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a0291c"
}
```

