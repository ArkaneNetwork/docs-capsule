---
description: 'Fetch your balance history, an overview of sales, purchases and commissions'
---

# Get user balance history

{% api-method method="get" host="https://api.arkane.market" path="/user/credits/history" %}
{% api-method-summary %}
Get user balance history
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
https://api.arkane.market/user/credits/history
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "date": "2021-06-03T12:26:50.091337",
            "userId": "4917b6fa-2657-4bdd-b8e8-fa5dd8bd4057",
            "type": "PURCHASE",
            "reference": {
                "id": "1e283f73-9b62-47d8-bb64-4495f83d4505",
                "type": "OFFER"
            },
            "gross": -12,
            "net": -12,
            "fees": []
        }
    ]
}
```

{% hint style="info" %}
**Gross**: The total amount of the offer  
**Net**: The value that impacts your balance  
**Fees**: The difference between gross and net. Fees that are taken by the market and the collection owner
{% endhint %}



