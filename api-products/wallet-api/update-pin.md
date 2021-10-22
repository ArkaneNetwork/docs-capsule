---
description: How to update the pin of a wallet
---

# Update wallet PIN

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<WALLET_ID>/security" method="patch" summary="Update wallet pin" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="newPincode" type="string" %}
New pin
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
Current pin
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
PATCH : https://api.arkane.network/api/wallets/<WALLET_ID>/security
```
{% endswagger-response %}
{% endswagger %}

## Example&#x20;

#### Request&#x20;

```javascript
PATCH : https://api.arkane.network/api/wallets/944124ed-305d-4e56-a0fd-bce1c7f1537c/security
```

#### Request Body

```javascript
{
  "pincode" : "1111",
  "newPincode" : "1234"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "944124ed-305d-4e56-a0fd-bce1c7f1537c",
        "address": "0x5f6EadB01E6E130634850cDC9071862eD2607775",
        "walletType": "UNRECOVERABLE_WHITE_LABEL",
        "secretType": "ETHEREUM",
        "createdAt": "2021-01-22T19:22:29.252188",
        "archived": false,
        "alias": "graceful_panda",
        "description": "My first unrecoverable wallet",
        "primary": false,
        "hasCustomPin": true,
        "identifier": "type=unrecoverable",
        "balance": {
            "available": true,
            "secretType": "ETHEREUM",
            "balance": 0.0,
            "gasBalance": 0.0,
            "symbol": "ETH",
            "gasSymbol": "ETH",
            "rawBalance": "0",
            "rawGasBalance": "0",
            "decimals": 18
        }
    }
}
```
