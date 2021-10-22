---
description: How to import an existing wallet
---

# Import a wallet

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/import" method="post" summary=" Import using private key" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="walletType" type="string" %}
Make it recoverable or not
{% endswagger-parameter %}

{% swagger-parameter in="body" name="importWalletType" type="string" %}
Type of import (eg. MATIC_PRIVATE_KEY)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN to encrypt the wallet with
{% endswagger-parameter %}

{% swagger-parameter in="body" name="privateKey" type="string" %}
Private key of the existing wallet
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/import" method="post" summary="Import using keystore" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN to encrypt the wallet with
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletType" type="string" %}
Make it recoverable or not
{% endswagger-parameter %}

{% swagger-parameter in="body" name="importWalletType" type="string" %}
Type of import (eg. MATIC_KEYSTORE)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="keystore" type="string" %}
JSON file that represents the wallet (warning: this is a string field so make sure the JSON body is escaped properly)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" type="string" %}
The password of the keystore
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/import" method="post" summary="Import using WIF" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="walletType" type="string" %}
Make it recoverable or not
{% endswagger-parameter %}

{% swagger-parameter in="body" name="importWalletType" type="string" %}
Type of import (eg. BITCOIN_WIF)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN to encrypt the wallet with
{% endswagger-parameter %}

{% swagger-parameter in="body" name="wif" type="string" %}
The wif (wallet import format) 
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/import" method="post" summary="Import from other secret type (blockchain)" %}
{% swagger-description %}
Using this endpoint, it is possible to use the same wallet (address) for a different blockchain. Currently it is only possible to import from ETHEREUM to MATIC, BSC and vice versa.
{% endswagger-description %}

{% swagger-parameter in="body" name="walletType" type="string" %}
Make it recoverable or not
{% endswagger-parameter %}

{% swagger-parameter in="body" name="importWalletType" type="string" %}
Must be: MIGRATION
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN for the wallet
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" type="string" %}
The ID of the wallet you want to import into another secret type
{% endswagger-parameter %}

{% swagger-parameter in="body" name="to" type="object" %}
Destination SecretType (blockchain), ex: MATIC
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "success": true,
    "result": {
        "id": "08aa6c62-509c-4999-914b-f649c1812eb1",
        "address": "0x5b0BB5d41A3e24222257625e746aFc2275c78315",
        "secretType": "MATIC",
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
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
For exporting a wallet please have a look at [`Export a wallet`](export-a-wallet.md).
{% endhint %}

## Object Types

{% content-ref url="../../deep-dive-1/object-reference/wallettype.md" %}
[wallettype.md](../../deep-dive-1/object-reference/wallettype.md)
{% endcontent-ref %}

{% content-ref url="../../deep-dive-1/object-reference/importwallettype.md" %}
[importwallettype.md](../../deep-dive-1/object-reference/importwallettype.md)
{% endcontent-ref %}

{% content-ref url="../../deep-dive-1/object-reference/secrettype.md" %}
[secrettype.md](../../deep-dive-1/object-reference/secrettype.md)
{% endcontent-ref %}

