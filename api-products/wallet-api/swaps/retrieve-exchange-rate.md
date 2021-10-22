---
description: Endpoint to gather detailed information about a potential swap
---

# 2 - Retrieve exchange rate

This endpoint returns information about the expected result of the swap. It provides the expected output amount, as well gives information about the slippage, and fee involved for that specific swap.

{% swagger baseUrl="https://api.arkane.network" path="/api/swaps/rates" method="get" summary="Get exchange rate" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="fromSecretType" type="string" %}
Blockchain to use
{% endswagger-parameter %}

{% swagger-parameter in="query" name="toSecretType" type="string" %}
Blockchain to use
{% endswagger-parameter %}

{% swagger-parameter in="query" name="fromToken" type="string" %}
Token address of the source token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="toToken" type="string" %}
Token address of the destination token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="amount" type="number" %}
Amount to swap
{% endswagger-parameter %}

{% swagger-parameter in="query" name="orderType" type="string" %}
SELL
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "success": true,
    "result": {
        "exchangeRates": [
            {
                "exchange": "ONE_INCH",
                "orderType": "SELL",
                "inputAmount": 1.000000000000000000,
                "outputAmount": 0.773096508478042589,
                "slippage": 0.05,
                "fee": 3.0
            }
        ],
        "bestRate": {
            "exchange": "ONE_INCH",
            "orderType": "SELL",
            "inputAmount": 1.000000000000000000,
            "outputAmount": 0.773096508478042589,
            "slippage": 0.05,
            "fee": 3.0
        }
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
https://api.arkane.network/api/swaps/rates?fromSecretType=MATIC&toSecretType=MATIC&fromToken=0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee&toToken=0x348e62131fce2f4e0d5ead3fe1719bc039b380a9&amount=1&orderType=SELL
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "exchangeRates": [
            {
                "exchange": "ONE_INCH",
                "orderType": "SELL",
                "inputAmount": 1.000000000000000000,
                "outputAmount": 0.773096508478042589,
                "slippage": 0.05,
                "fee": 3.0
            }
        ],
        "bestRate": {
            "exchange": "ONE_INCH",
            "orderType": "SELL",
            "inputAmount": 1.000000000000000000,
            "outputAmount": 0.773096508478042589,
            "slippage": 0.05,
            "fee": 3.0
        }
    }
}
```
