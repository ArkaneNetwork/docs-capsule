---
description: Retrieve the USDC deposit address for topping up your account
---

# Get deposit address

{% swagger baseUrl="https://api.arkane.market" path="/user/deposit-addresses" method="get" summary="Get deposit address" %}
{% swagger-description %}

{% endswagger-description %}

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
https://api.arkane.market/user/deposit-addresses
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

{% hint style="info" %}
When the response is empty you can create a deposit address by using the [Create deposit address](create-deposit-address.md) endpoint.
{% endhint %}
