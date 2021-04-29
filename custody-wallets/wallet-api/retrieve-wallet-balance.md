---
description: How to retrieve the native balance of a wallet
---

# Retrieve wallet balance

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/<walletId>/balance" %}
{% api-method-summary %}
Get native balance
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletId" type="string" required=true %}
ID of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "available": true,
        "secretType": "MATIC",
        "balance": 0.089979,
        "gasBalance": 0.089979,
        "symbol": "MATIC",
        "gasSymbol": "MATIC",
        "rawBalance": "89979000000000000",
        "rawGasBalance": "89979000000000000",
        "decimals": 18
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": {
        "available": true,
        "secretType": "MATIC",
        "balance": 0.089979,
        "gasBalance": 0.089979,
        "symbol": "MATIC",
        "gasSymbol": "MATIC",
        "rawBalance": "89979000000000000",
        "rawGasBalance": "89979000000000000",
        "decimals": 18
    }
}
```

## 

