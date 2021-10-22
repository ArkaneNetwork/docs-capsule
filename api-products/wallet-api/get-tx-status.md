---
description: >-
  Get the status of a specific transaction. Returns UNKNOWN when the specific
  chain is not supported yet.
---

# Get Tx status

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/:secretType/:transactionHash/status" method="get" summary="Get the status of a transaction" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="transactionHash" type="string" %}
The transaction hash (id)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="secretType" type="string" %}
Chain (Ethereum, MATIC, BSC,...)
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```java
{
    "success": true,
    "result": {
        "hash": "0x586b8c4d1f2a3d5760b6290825149cd1319c91b65b258e3f8a8fb432e6c0cbe3",
        "status": "SUCCEEDED",
        "confirmations": 109092,
        "blockHash": "0xcb0733d4c84a158863723c3f4d45da069b9acb2b361cb77d5ec376e53733c40f",
        "blockNumber": 8538423,
        "nonce": 118,
        "gas": 200000,
        "gasUsed": 64484,
        "gasPrice": 74800000000,
        "logs": [
            {
                "logIndex": 1,
                "data": "0x",
                "type": null,
                "topics": [
                    "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
                    "0x00000000000000000000000039069fb544c7e25122b8a54cd7b982d34d11e470",
                    "0x0000000000000000000000006156174da796228b376e3e58506194543cfbca38",
                    "0x0000000000000000000000000000000000000000000000000000000000000014"
                ]
            }
        ],
        "from": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
        "to": "0x1ec84ea808b8c30483c6bb3a82f4315f3007beac"
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Example&#x20;

#### Request&#x20;

```javascript
GET : https://api.arkane.network/api/transactions/ETHEREUM/0x586b8c4d1f2a3d5760b6290825149cd1319c91b65b258e3f8a8fb432e6c0cbe3/status
```

#### Response

```java
{
    "success": true,
    "result": {
        "hash": "0x586b8c4d1f2a3d5760b6290825149cd1319c91b65b258e3f8a8fb432e6c0cbe3",
        "status": "SUCCEEDED",
        "confirmations": 109092,
        "blockHash": "0xcb0733d4c84a158863723c3f4d45da069b9acb2b361cb77d5ec376e53733c40f",
        "blockNumber": 8538423,
        "nonce": 118,
        "gas": 200000,
        "gasUsed": 64484,
        "gasPrice": 74800000000,
        "logs": [
            {
                "logIndex": 1,
                "data": "0x",
                "type": null,
                "topics": [
                    "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
                    "0x00000000000000000000000039069fb544c7e25122b8a54cd7b982d34d11e470",
                    "0x0000000000000000000000006156174da796228b376e3e58506194543cfbca38",
                    "0x0000000000000000000000000000000000000000000000000000000000000014"
                ]
            }
        ],
        "from": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
        "to": "0x1ec84ea808b8c30483c6bb3a82f4315f3007beac"
    }
}
```
