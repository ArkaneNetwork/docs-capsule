---
description: Fetch your balance
---

# Get user balance

{% api-method method="get" host="https://api.arkane.market" path="/user/credits" %}
{% api-method-summary %}
Get user balance/credits
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "balance": 25132.46,
        "lockedBalance": 0
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

