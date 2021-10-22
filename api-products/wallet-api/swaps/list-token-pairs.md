---
description: Fetch a list of available token pairs
---

# 1 - Retrieve token pairs

Get the available token pairs supported by our endpoint. The result set depends on the blockchain the wallet (`walletId`) is hosted on. If you feel you are missing a token pair, please contact us and we will look into making that available for you.

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/:walletId/swaps/pairs" method="get" summary="Get possible pairs" %}
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
            "from": {
                "secretType": "MATIC",
                "symbol": "MATIC",
                "tokenAddress": "0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
            },
            "to": {
                "secretType": "MATIC",
                "symbol": "USDT",
                "tokenAddress": "0xc2132d05d31c914a87c6611c10748aeb04b58e8f"
            }
        },
        {
            "from": {
                "secretType": "MATIC",
                "symbol": "MATIC",
                "tokenAddress": "0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
            },
            "to": {
                "secretType": "MATIC",
                "symbol": "AAVE",
                "tokenAddress": "0xd6df932a45c0f255f85145f286ea0b292b21c90b"
            }
        }
    ]
}


```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Note:** The token pairs will be automatically filtered based on the blockchain that is hosting the wallet. If the wallet is on Ethereum, the list will only display tokens that are available for swapping on the Ethereum blockchain.

Currently, the swap endpoints support Ethereum, Polygon (Matic), and BSC (Binance Smart Chain).
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.network/api/wallets/b97e9e8b-035c-40a0-bac0-96b07fc0444a/swaps/pairs
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "from": {
                "secretType": "MATIC",
                "symbol": "MATIC",
                "tokenAddress": "0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
            },
            "to": {
                "secretType": "MATIC",
                "symbol": "USDT",
                "tokenAddress": "0xc2132d05d31c914a87c6611c10748aeb04b58e8f"
            }
        },
        {
            "from": {
                "secretType": "MATIC",
                "symbol": "MATIC",
                "tokenAddress": "0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
            },
            "to": {
                "secretType": "MATIC",
                "symbol": "AAVE",
                "tokenAddress": "0xd6df932a45c0f255f85145f286ea0b292b21c90b"
            }
        }
    ]
}
```
