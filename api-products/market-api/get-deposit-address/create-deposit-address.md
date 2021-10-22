---
description: Endpoint to generate a deposit address for your user.
---

# Create deposit address

{% swagger baseUrl="https://api.arkane.market" path="/user/deposit-addresses" method="post" summary="Create deposit address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="secretType" type="string" %}
ETHEREUM
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
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
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
POST https://api.arkane.market/user/deposit-addresses
```

#### Request Body

```javascript
{
    "secretType": "ETHEREUM"
}
```

#### Response

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
