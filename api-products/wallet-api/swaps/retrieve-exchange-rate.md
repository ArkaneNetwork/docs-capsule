---
description: Endpoint to gather detailed information about a potential swap
---

# 2 - Retrieve exchange rate

This endpoint returns information about the expected result of the swap. It provides the expected output amount, as well gives information about the slippage, and fee involved for that specific swap.

{% api-method method="get" host="https://api.arkane.network" path="/api/swaps/rates" %}
{% api-method-summary %}
Get exchange rate
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="fromSecretType" type="string" required=true %}
Blockchain to use
{% endapi-method-parameter %}

{% api-method-parameter name="toSecretType" type="string" required=true %}
Blockchain to use
{% endapi-method-parameter %}

{% api-method-parameter name="fromToken" type="string" required=true %}
Token address of the source token
{% endapi-method-parameter %}

{% api-method-parameter name="toToken" type="string" required=true %}
Token address of the destination token
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="number" required=true %}
Amount to swap
{% endapi-method-parameter %}

{% api-method-parameter name="orderType" type="string" required=true %}
SELL
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

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

