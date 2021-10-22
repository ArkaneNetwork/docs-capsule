---
description: Retrieve a set of wallets using a common identifier
---

# Retrieve a wallet by identifier

{% swagger baseUrl="https://api-arkane.network" path="/api/wallets?identifier=<COMMON_IDENTIFIER>" method="get" summary="Get wallet by identifier" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="identifier" type="string" %}
Identifier to fetch a single or group of wallets
{% endswagger-parameter %}

{% swagger-response status="200" description="The result of the call and a group of wallets" %}
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
            "identifier": "user_id=ABC123",
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
            "identifier": "user_id=ABC123",
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
For retrieving all wallets or a or specific wallet it is recommended to use [`Get wallets`](untitled.md) or [`Get wallet`](get-wallet.md).
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.network/api/wallets?identifier=user_id=ABC123
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
            "identifier": "user_id=ABC123",
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
            "identifier": "user_id=ABC123",
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
