---
description: Fetch your balance
---

# Get user balance

{% swagger baseUrl="https://api.arkane.market" path="/user/credits" method="get" summary="Get user balance/credits" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "success": true,
    "result": {
        "balance": 25132.46,
        "lockedBalance": 0
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
https://api.arkane.market/user/credits
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "balance": 25132.46,
        "lockedBalance": 0
    }
}
```
