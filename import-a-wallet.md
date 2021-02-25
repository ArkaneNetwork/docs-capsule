---
description: How to import an existing wallet using a private key
---

# Import a wallet

{% api-method method="post" host="https://api.arkane.network" path="/api/wallets/import" %}
{% api-method-summary %}
Import a wallet
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="walletType" type="string" required=true %}
Make it recoverable or not
{% endapi-method-parameter %}

{% api-method-parameter name="importWalletType" type="string" required=true %}
Type of import \(eg. MATIC\_PRIVATE\_KEY\)
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
PIN to encrypt the wallet with
{% endapi-method-parameter %}

{% api-method-parameter name="privateKey" type="string" required=true %}
Private key of the existing wallet
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "id": "08aa6c62-509c-4999-914b-f649c1812eb1",
        "address": "0x5b0BB5d41A3e24222257625e746aFc2275c78315",
        "secretType": "BSC",
        "walletType": "WHITE_LABEL",
        "createdAt": null,
        "archived": false,
        "alias": "white_hat_dogfish",
        "description": "White hat Dogfish",
        "primary": true,
        "hasCustomPin": true,
        "balance": {
            "available": true,
            "secretType": "BSC",
            "balance": 0.0,
            "gasBalance": 0.0,
            "symbol": "BNB",
            "gasSymbol": "BNB",
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

{% hint style="info" %}
For exporting a wallet please have a look at [`Export a wallet`](export-a-wallet.md).
{% endhint %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "08aa6c62-509c-4999-914b-f649c1812eb1",
        "address": "0x5b0BB5d41A3e24222257625e746aFc2275c78315",
        "secretType": "BSC",
        "walletType": "WHITE_LABEL",
        "createdAt": null,
        "archived": false,
        "alias": "white_hat_dogfish",
        "description": "White hat Dogfish",
        "primary": true,
        "hasCustomPin": true,
        "balance": {
            "available": true,
            "secretType": "BSC",
            "balance": 0.0,
            "gasBalance": 0.0,
            "symbol": "BNB",
            "gasSymbol": "BNB",
            "rawBalance": "0",
            "rawGasBalance": "0",
            "decimals": 18
        }
    }
}
```

## Object Types

{% page-ref page="capsule-advanced/object-reference/wallettype.md" %}


