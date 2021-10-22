---
description: Retrieve a single wallet using its unique id
---

# Retrieve a wallet

{% swagger baseUrl=" https://api.arkane.network" path="/api/wallets/<wallet_id>" method="get" summary="Get wallet" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="wallet id" type="string" %}
The id of the wallet you want to fetch.
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
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
        }
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
For retrieving all wallets or a set of wallets based on a common identifier it is recommended to use [`Get wallets`](untitled.md) or [`Get wallet by id`](get-wallet-by-id.md).
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.network/api/wallets/6ddcbcc3-e242-4bb5-b4f3-3913ccba3e8d
```

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
        }
}
```

##
