---
description: Retrieve the NFT contract information based on the contract address
---

# Get NFT contract

{% api-method method="get" host="https://<chain>-azrael.arkane.network" path="/contracts/:tokenContract" %}
{% api-method-summary %}
Get token contract
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="tokenContract" type="string" required=true %}
Address of the token contract
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
    "contractType": "ERC_721",
    "name": "Neon District Season One Item",
    "symbol": "NDITEM1"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

```javascript
https://matic-azrael.arkane.network/contracts/0x7227e371540cf7b8e512544ba6871472031f3335
```

#### Response

```javascript
{
    "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
    "contractType": "ERC_721",
    "name": "Neon District Season One Item",
    "symbol": "NDITEM1"
}
```

