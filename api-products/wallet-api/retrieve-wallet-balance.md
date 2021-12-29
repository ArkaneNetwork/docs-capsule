---
description: How to retrieve the native balance of a wallet
---

# Retrieve wallet balance

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/:walletId/balance" method="get" summary="Get native balance by wallet id" %}
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

{% swagger method="get" path="/api/wallets/:secretType/:walletAddress/balance" baseUrl="https://api.arkane.network" summary="Get native balance by secret type and wallet address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="secretType" type="SecretType" required="true" %}
Indication on which chain the balance should be fetched
{% endswagger-parameter %}

{% swagger-parameter in="path" name="walletAddress" required="true" %}
The address of the wallet
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "success": true,
    "result": {
        "available": true,
        "secretType": "MATIC",
        "balance": 6537.995854438881,
        "gasBalance": 6537.995854438881,
        "symbol": "MATIC",
        "gasSymbol": "MATIC",
        "rawBalance": "6537995854438880776000",
        "rawGasBalance": "6537995854438880776000",
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
