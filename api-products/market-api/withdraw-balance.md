---
description: Endpoint to withdraw your balance/credits in USDC to an Ethereum wallet
---

# Withdraw balance

{% api-method method="post" host="https://api.arkane.market" path="/user/deposit-addresses" %}
{% api-method-summary %}
Create deposit address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="secretType" type="string" required=true %}
ETHEREUM
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

