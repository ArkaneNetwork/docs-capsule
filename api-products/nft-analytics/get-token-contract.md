---
description: Retrieve the NFT contract information based on the contract address
---

# Get NFT contract

{% swagger baseUrl="https://<chain>-azrael.arkane.network" path="/contracts/:tokenContract" method="get" summary="Get token contract" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="tokenContract" type="string" %}
Address of the token contract
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
    "contractType": "ERC_721",
    "name": "Neon District Season One Item",
    "symbol": "NDITEM1"
}
```
{% endswagger-response %}
{% endswagger %}

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
