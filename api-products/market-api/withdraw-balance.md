---
description: Endpoint to withdraw your balance/credits in USDC to an Ethereum wallet
---

# Withdraw balance

{% swagger baseUrl="https://api.arkane.market" path="/orders/usdc" method="post" summary="Create deposit address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="string" %}
Blockchain address which will receive the USDC
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
WITHDRAWAL
{% endswagger-parameter %}

{% swagger-parameter in="body" name="amount" type="integer" %}
Amount of USDC to withdraw
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
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
}
```
{% endswagger-response %}
{% endswagger %}

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
{
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
}
```
