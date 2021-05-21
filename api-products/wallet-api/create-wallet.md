---
description: How to create a new blockchain wallet
---

# Create wallet

{% api-method method="post" host="https://api.arkane.network" path="/api/wallet" %}
{% api-method-summary %}
Create wallet
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="walletType" type="string" required=true %}
Define if the wallet is recoverable or unrecoverable
{% endapi-method-parameter %}

{% api-method-parameter name="secretType" type="string" required=true %}
The blockchain on which to create the wallet
{% endapi-method-parameter %}

{% api-method-parameter name="identifier" type="string" required=false %}
An identifier that can be used to query or group wallets
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
A description to describe the wallet.
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
The pin that will encrypt and decrypt the wallet
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Status of the call and the wallet is returned.
{% endapi-method-response-example-description %}

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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Object Types

{% page-ref page="../../capsule-advanced/object-reference/secrettype.md" %}

{% page-ref page="../../capsule-advanced/object-reference/wallettype.md" %}

