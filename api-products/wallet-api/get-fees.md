---
description: 'Get the current fees (for EVM based chains: gasprice) for a certain chain'
---

# Get fees

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/{secretType}/fees" method="get" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="secretType" type="string" %}
The secret type
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the current fee for given chain. 
Warning: the resulting object structure can be different depending on given secretType" %}
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
{% endswagger-response %}
{% endswagger %}

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
