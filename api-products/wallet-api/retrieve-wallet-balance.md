---
description: How to retrieve the native balance of a wallet
---

# Retrieve wallet balance

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<walletId>/balance" method="get" summary="Get native balance" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="walletId" type="string" %}
ID of the wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

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
