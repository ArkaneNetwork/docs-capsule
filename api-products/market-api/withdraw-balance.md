---
description: Endpoint to withdraw your balance/credits in USDC to an Ethereum wallet
---

# Withdraw balance

{% api-method method="post" host="https://api.arkane.market" path="/orders/usdc" %}
{% api-method-summary %}
Create deposit address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="string" required=true %}
Blockchain address which will receive the USDC
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
WITHDRAWAL
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="integer" required=true %}
Amount of USDC to withdraw
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "userId": "7c344b6c-2a05-4597-95ce-9b48e07f8e50",
            "secretType": "ETHEREUM",
            "address": "0xa51b1d9f8715884647aea7c593e4ff3176aaac16"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

```javascript
POST https://api.arkane.market/orders/usdc
```

#### Request Body

```javascript
{
    "amount": 12.76,
    "type": "WITHDRAWAL",
    "address": "0xBf27d5e974B048eDEe25EC05c6fC264946aC3A33"
}
```

#### Response

```javascript

    "success": true,
    "result": {
        "id": "8d0d817c-3011-43ed-8feb-4cec99e6cd2c",
        "userId": "4917b6fa-2657-4bdd-b8e8-fa5dd8bd4057",
        "paymentProviderOrderId": "edb95c76-30e9-4f98-823b-e829cc073ea5",
        "paymentProcessor": "USDC",
        "quantity": 7.76,
        "handlingFee": 0,
        "marketFee": 5,
        "currency": "USDC",
        "status": "PENDING",
        "date": "2021-06-30T13:39:27.953792Z",
        "type": "WITHDRAWAL"
    }
```

