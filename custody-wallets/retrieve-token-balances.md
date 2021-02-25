---
description: How to retrieve the token balances for a wallet (ERC20 standard)
---

# Retrieve token balance

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens" %}
{% api-method-summary %}
Get all token balances
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
            "tokenAddress": "0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e",
            "rawBalance": "1000000000000000000",
            "balance": 1.0,
            "decimals": 18,
            "symbol": "TST",
            "logo": "https://img.arkane.network/tokens/matic/testnet/logos/0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e.png",
            "type": "ERC_20",
            "transferable": true
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens/<tokenAddress>" %}
{% api-method-summary %}
Get a specific token balance
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="tokenAddress" type="string" required=true %}
Token address
{% endapi-method-parameter %}

{% api-method-parameter name="walletId" type="string" required=true %}
ID of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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
            "tokenAddress": "0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e",
            "rawBalance": "1000000000000000000",
            "balance": 1.0,
            "decimals": 18,
            "symbol": "TST",
            "logo": "https://img.arkane.network/tokens/matic/testnet/logos/0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e.png",
            "type": "ERC_20",
            "transferable": true
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
            "tokenAddress": "0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e",
            "rawBalance": "1000000000000000000",
            "balance": 1.0,
            "decimals": 18,
            "symbol": "TST",
            "logo": "https://img.arkane.network/tokens/matic/testnet/logos/0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e.png",
            "type": "ERC_20",
            "transferable": true
        }
    ]
}
```



## 

