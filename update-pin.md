---
description: How to update the pin of a wallet
---

# Update wallet PIN

{% api-method method="patch" host="https://api.arkane.network" path="/api/wallets/<WALLET\_ID>/security" %}
{% api-method-summary %}
Update wallet pin
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="newPincode" type="string" required=true %}
New pin
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
Current pin
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
PATCH : https://api.arkane.network/api/wallets/<WALLET_ID>/security
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example 

#### Request 

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

