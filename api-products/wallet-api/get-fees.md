---
description: 'Get the current fees (for EVM based chains: gasprice) for a certain chain'
---

# Get fees

{% api-method method="get" host="https://api.arkane.network" path="/api/transactions/{secretType}/fees" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="secretType" type="string" required=false %}
The secret type
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the current fee for given chain.   
Warning: the resulting object structure can be different depending on given secretType
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "gasPrice": 21450000000,
            "defaultPrice": false
        },
        {
            "gasPrice": 21450000000,
            "defaultPrice": true
        },
        {
            "gasPrice": 25300000000,
            "defaultPrice": false
        },
        {
            "gasPrice": 29700000000,
            "defaultPrice": false
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Example

```javascript
GET : https://api.arkane.network/api/transactions/ETHEREUM/fees
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "gasPrice": 21450000000,
            "defaultPrice": false
        },
        {
            "gasPrice": 21450000000,
            "defaultPrice": true
        },
        {
            "gasPrice": 25300000000,
            "defaultPrice": false
        },
        {
            "gasPrice": 29700000000,
            "defaultPrice": false
        }
    ]
}
```

