---
description: Sign data using your wallet
---

# Signatures

{% api-method method="post" host="https://api.arkane.network" path="/api/signatures" %}
{% api-method-summary %}
Sign a message \(arbitrary data\)
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

{% hint style="info" %}
🧙 The signatures endpoint supports the [EIP-712](https://eips.ethereum.org/EIPS/eip-712) standard, Ethereum typed structured data hashing and signing. This EIP aims to improve the usability of off-chain message signing for use on-chain.
{% endhint %}

{% api-method method="post" host="https://api.arkane.network" path="/api/signatures" %}
{% api-method-summary %}
Sign an EIP712 message
{% endapi-method-summary %}

{% api-method-description %}
This api allows you to sign EIP712 messages
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="signatureRequest.data" type="string" required=true %}
The JSON of the EIP712 message to sign
{% endapi-method-parameter %}

{% api-method-parameter name="signatureRequest.type" type="string" required=true %}
The signature type, in this case: EIP712
{% endapi-method-parameter %}

{% api-method-parameter name="signatureRequest.secretType" type="string" required=true %}
The secret type where you want to sign
{% endapi-method-parameter %}

{% api-method-parameter name="signatureRequest.walletId" type="string" required=true %}
The id of the wallet of which you want to sign
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
The pincode for the wallet
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
        "type": "HEX_SIGNATURE",
        "r": "0xc3708e09824e67af571b0c4d2d9a98c4ec5eb2831946674da7db5d6bc1a35635",
        "s": "0x53174e2c71cdac33b447974f54cddcf63bd2644106edad6ee53665c032f370b1",
        "v": "0x1b",
        "signature": "0xc3708e09824e67af571b0c4d2d9a98c4ec5eb2831946674da7db5d6bc1a3563553174e2c71cdac33b447974f54cddcf63bd2644106edad6ee53665c032f370b11b"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

```javascript
POST : https://api.arkane.network/api/signatures
```

#### Request Body

```javascript
{
    "pincode": 1234,
    "signatureRequest": {
        "type": "EIP712",
        "secretType": "ETHEREUM",
        "walletId": "d6c73e54-dce3-4ec4-974f-93942e177d5b",
        "data": {
            "types": {
                "EIP712Domain": [
                    {
                        "name": "name",
                        "type": "string"
                    },
                    {
                        "name": "version",
                        "type": "string"
                    },
                    {
                        "name": "chainId",
                        "type": "uint256"
                    },
                    {
                        "name": "verifyingContract",
                        "type": "address"
                    },
                    {
                        "name": "salt",
                        "type": "bytes32"
                    }
                ],
                "Bid": [
                    {
                        "name": "amount",
                        "type": "uint256"
                    },
                    {
                        "name": "bidder",
                        "type": "Identity"
                    }
                ],
                "Identity": [
                    {
                        "name": "userId",
                        "type": "uint256"
                    },
                    {
                        "name": "wallet",
                        "type": "address"
                    }
                ]
            },
            "domain": {
                "name": "My amazing dApp",
                "version": "2",
                "chainId": 1,
                "verifyingContract": "0x1C56346CD2A2Bf3202F771f50d3D14a367B48070",
                "salt": "0xf2d857f4a3edcb9b78b4d503bfe733db1e3f6cdc2b7971ee739626c97e86a558"
            },
            "primaryType": "Bid",
            "message": {
                "amount": 100,
                "bidder": {
                    "userId": 323,
                    "wallet": "0x3333333333333333333333333333333333333333"
                }
            }
        }
    }
}

```

#### Response

```javascript
{
    "success": true,
    "result": {
        "type": "HEX_SIGNATURE",
        "r": "0xc3708e09824e67af571b0c4d2d9a98c4ec5eb2831946674da7db5d6bc1a35635",
        "s": "0x53174e2c71cdac33b447974f54cddcf63bd2644106edad6ee53665c032f370b1",
        "v": "0x1b",
        "signature": "0xc3708e09824e67af571b0c4d2d9a98c4ec5eb2831946674da7db5d6bc1a3563553174e2c71cdac33b447974f54cddcf63bd2644106edad6ee53665c032f370b11b"
    }
}
```

