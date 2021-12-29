---
description: How to retrieve the token balances for a wallet (ERC20 standard)
---

# Retrieve token balance

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens" method="get" summary="Get all token balances by wallet id" %}
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

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/<walletId>/balance/tokens/<tokenAddress>" method="get" summary="Get a specific token balance by wallet id" %}
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

{% swagger method="get" path="/:secretType/:walletAddress/balance/tokens" baseUrl="https://api.arkane.network" summary="Get all token balances by secret type and wallet address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" required="true" name="secretType" type="SecretType" %}
Parameter to indicate on which chain the token balances should be fetched
{% endswagger-parameter %}

{% swagger-parameter in="path" name="waletAddress" type="String" required="true" %}
The address of the wallet to fetch token balances for
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "success": true,
    "result": [
        {
            "tokenAddress": "0x01b98a3f1766ff8248bf33b05213f411d3272261",
            "rawBalance": "50000000000",
            "balance": 50000.0,
            "decimals": 6,
            "symbol": "USDC",
            "logo": "https://logos.covalenthq.com/tokens/80001/0x01b98a3f1766ff8248bf33b05213f411d3272261.png",
            "type": "ERC20",
            "transferable": true,
            "name": "USD Coin"
        },
        {
            "tokenAddress": "0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e",
            "rawBalance": "60000000000000000",
            "balance": 0.06,
            "decimals": 18,
            "symbol": "TST",
            "logo": "https://logos.covalenthq.com/tokens/80001/0x2d7882bedcbfddce29ba99965dd3cdf7fcb10a1e.png",
            "type": "ERC20",
            "transferable": true,
            "name": "Test Token"
        },
        {
            "tokenAddress": "0x4354ede79651b3627332faad1a4ceb001d005ce9",
            "rawBalance": "990000000000000000000",
            "balance": 990.0,
            "decimals": 18,
            "symbol": "BNA",
            "logo": "https://logos.covalenthq.com/tokens/80001/0x4354ede79651b3627332faad1a4ceb001d005ce9.png",
            "type": "ERC20",
            "transferable": true,
            "name": "Banana"
        },
        {
            "tokenAddress": "0xfe4f5145f6e09952a5ba9e956ed0c25e3fa4c7f1",
            "rawBalance": "2000000000000000000",
            "balance": 2.0,
            "decimals": 18,
            "symbol": "DERC20",
            "logo": "https://logos.covalenthq.com/tokens/80001/0xfe4f5145f6e09952a5ba9e956ed0c25e3fa4c7f1.png",
            "type": "ERC20",
            "transferable": true,
            "name": "Dummy ERC20"
        }
    ]
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/:secretType/:walletAddress/balance/tokens/:tokenAddress" baseUrl="https://api.arkane.network" summary="Get a specific token balance by secret type and wallet address" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="secretType" type="SecretType" required="true" %}
Parameter to indicate on which chain the token balance should be fetched
{% endswagger-parameter %}

{% swagger-parameter in="path" name="walletAddress" type="String" required="true" %}
The address of the wallet to fetch token balance for
{% endswagger-parameter %}

{% swagger-parameter in="path" required="true" name="tokenAddress" type="String" %}
Address of the token (contract) to fetch the balance for
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "success": true,
    "result": {
        "tokenAddress": "0x01b98a3f1766ff8248bf33b05213f411d3272261",
        "rawBalance": "50000000000",
        "balance": 50000.0,
        "decimals": 6,
        "symbol": "USDC",
        "logo": null,
        "type": "ERC20",
        "transferable": true,
        "name": "Venly"
    }
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
