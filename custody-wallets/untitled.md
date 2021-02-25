---
description: Retrieve all the wallets
---

# Retrieve all wallets

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets" %}
{% api-method-summary %}
Get all wallets
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "id": "6ddcbcc3-e242-4bb5-b4f3-3913ccba3e8d",
            "address": "0xd7A742EFa8f3b24bc39EF288C2eEf3f1F6956a60",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:17:42.301523",
            "archived": false,
            "alias": "magnetic_horse",
            "description": "Just another test Wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet",
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
        },
        {
            "id": "7db27653-1ad0-4ce0-b5a5-82fad6751a9b",
            "address": "0xEe561aCF81603353F9a9028D354855978D8825aA",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:38:56.278746",
            "archived": false,
            "alias": "ingenious_rook",
            "description": "2nd wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet2",
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
        },
        {
            "id": "fa910695-4c20-4f82-b5e7-069b0260e03a",
            "address": "0x208A00ebedA2419eE9B81AE63e806750Da6a6109",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:34:42.696229",
            "archived": false,
            "alias": "ravishing_beetle",
            "description": "2nd wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet2",
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
        },
        {
            "id": "7fe12186-964e-431e-ad71-7830b36d3d3b",
            "address": "0x5f6EadB01E6E130634850cDC9071862eD2607775",
            "walletType": "UNRECOVERABLE_WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-22T19:22:29.252188",
            "archived": false,
            "alias": "graceful_panda",
            "description": "My first unrecoverable wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "type=unrecoverable",
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
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
For retrieving a specific wallet it is recommended to use [`Get wallet`](get-wallet.md) or [`Get wallet by id`](get-wallet-by-id.md).
{% endhint %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "id": "6ddcbcc3-e242-4bb5-b4f3-3913ccba3e8d",
            "address": "0xd7A742EFa8f3b24bc39EF288C2eEf3f1F6956a60",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:17:42.301523",
            "archived": false,
            "alias": "magnetic_horse",
            "description": "Just another test Wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet",
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
        },
        {
            "id": "7db27653-1ad0-4ce0-b5a5-82fad6751a9b",
            "address": "0xEe561aCF81603353F9a9028D354855978D8825aA",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:38:56.278746",
            "archived": false,
            "alias": "ingenious_rook",
            "description": "2nd wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet2",
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
        },
        {
            "id": "fa910695-4c20-4f82-b5e7-069b0260e03a",
            "address": "0x208A00ebedA2419eE9B81AE63e806750Da6a6109",
            "walletType": "WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-14T13:34:42.696229",
            "archived": false,
            "alias": "ravishing_beetle",
            "description": "2nd wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "arkane-created-wallet2",
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
        },
        {
            "id": "7fe12186-964e-431e-ad71-7830b36d3d3b",
            "address": "0x5f6EadB01E6E130634850cDC9071862eD2607775",
            "walletType": "UNRECOVERABLE_WHITE_LABEL",
            "secretType": "ETHEREUM",
            "createdAt": "2021-01-22T19:22:29.252188",
            "archived": false,
            "alias": "graceful_panda",
            "description": "My first unrecoverable wallet",
            "primary": false,
            "hasCustomPin": true,
            "identifier": "type=unrecoverable",
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
    ]
}
```

## 

