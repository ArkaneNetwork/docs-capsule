---
description: How to create a new blockchain wallet
---

# Create a wallet

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets" method="post" summary="Create wallet" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="walletType" type="string" %}
Define if the wallet is recoverable or unrecoverable
{% endswagger-parameter %}

{% swagger-parameter in="body" name="secretType" type="string" %}
The blockchain on which to create the wallet
{% endswagger-parameter %}

{% swagger-parameter in="body" name="identifier" type="string" %}
An identifier that can be used to query or group wallets
{% endswagger-parameter %}

{% swagger-parameter in="body" name="description" type="string" %}
A description to describe the wallet.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
The pin that will encrypt and decrypt the wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="Status of the call and the wallet is returned." %}
```javascript
{
    "success": true,
    "result": {
        "id": "f266a6e1-7e82-4d41-9aa2-41c079e72d09",
        "address": "0xf3e2C07F7ED3f45a24f2803c493080b21013f77c",
        "walletType": "WHITE_LABEL",
        "secretType": "ETHEREUM",
        "createdAt": "2021-01-15T14:45:13.265314",
        "archived": false,
        "alias": "tantalizing_horse",
        "description": "Just another test Wallet",
        "primary": false,
        "hasCustomPin": true,
        "identifier" : "user_id=ABC123"
        "balance": {
            "available": true,
            "secretType": "ETHEREUM",
            "balance": 0.0,
            "gasBalance": 0.0,
            "symbol": "ETH",
            "gasSymbol": "ETH",
            "rawBalance": "0",
            "rawGasBalance": "0",
            "decimals": 18
        }
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Object Types

{% content-ref url="../../deep-dive-1/object-reference/secrettype.md" %}
[secrettype.md](../../deep-dive-1/object-reference/secrettype.md)
{% endcontent-ref %}

{% content-ref url="../../deep-dive-1/object-reference/wallettype.md" %}
[wallettype.md](../../deep-dive-1/object-reference/wallettype.md)
{% endcontent-ref %}
