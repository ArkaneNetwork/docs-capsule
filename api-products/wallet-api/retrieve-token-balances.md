---
description: How to retrieve the token balances for a wallet (ERC20 standard)
---

# Retrieve token balance

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens" method="get" summary="Get all token balances" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="walletId" type="string" %}
ID of the wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens/<tokenAddress>" method="get" summary="Get a specific token balance" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="tokenAddress" type="string" %}
Token address
{% endswagger-parameter %}

{% swagger-parameter in="path" name="walletId" type="string" %}
ID of the wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

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
