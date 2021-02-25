---
description: How to retrieve non-fungible tokens for a wallet.
---

# Retrieve non-fungible tokens

NFTs can be queried either by wallet ID or by wallet address, if required multiple NFT contract addresses can be passed as a query parameter to act as a filter. 

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/<walletId>/nonfungibles" %}
{% api-method-summary %}
Get NFTs by wallet ID
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletId" type="string" required=true %}
ID of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="contract-addresses" type="string" required=false %}
When set, the result will only contain tokens of these NFT contract addresses. Multiple values can be set.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "description": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
            "url": null,
            "backgroundColor": null,
            "imageUrl": null,
            "imagePreviewUrl": null,
            "imageThumbnailUrl": null,
            "animationUrl": null,
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men",
                "description": null,
                "address": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155"
            },
            "attributes": null
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/MATIC/<walletAddress>/nonfungibles" %}
{% api-method-summary %}
Get NFTs by wallet address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletAddress" type="string" required=true %}
Blockchain address of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="contract-addresses" type="string" required=false %}
When set, the result will only contain tokens of these NFT contract addresses. Multiple values can be set.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "description": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
            "url": null,
            "backgroundColor": null,
            "imageUrl": null,
            "imagePreviewUrl": null,
            "imageThumbnailUrl": null,
            "animationUrl": null,
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men",
                "description": null,
                "address": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155"
            },
            "attributes": null
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "description": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
            "url": null,
            "backgroundColor": null,
            "imageUrl": null,
            "imagePreviewUrl": null,
            "imageThumbnailUrl": null,
            "animationUrl": null,
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men",
                "description": null,
                "address": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155"
            },
            "attributes": null
        }
    ]
}
```

