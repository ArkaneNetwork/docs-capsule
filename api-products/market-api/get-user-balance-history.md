---
description: Fetch your balance history, an overview of sales, purchases and commissions
---

# Get user balance history

{% swagger baseUrl="https://api.arkane.market" path="/user/credits/history" method="get" summary="Get user balance history" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "success": true,
    "result": [
        {
            "date": "2021-06-22T19:44:35.896220",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "2367d75e-7e52-45e1-98b7-3ac6ded9e7f1",
                "type": "ORDER"
            },
            "gross": 1.00,
            "net": 1.00,
            "fees": []
        },
        {
            "date": "2021-06-15T20:59:05.609988",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "935870c1-82d5-4f8a-a869-61af6367cda9",
                "type": "ORDER"
            },
            "gross": 100,
            "net": 100,
            "fees": []
        },
        {
            "date": "2021-06-15T20:57:04.647446",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "e95e4717-b720-4560-984b-8847ef37b641",
                "type": "ORDER"
            },
            "gross": 10,
            "net": 10,
            "fees": []
        },
        {
            "date": "2021-06-09T15:14:16.335428",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "a71940cf-18cc-4289-bcad-ddbbfe2b94bf",
                "type": "OFFER"
            },
            "gross": 1,
            "net": 0.88,
            "fees": [
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.0,
                    "amount": -0.02
                },
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.0,
                    "amount": -0.10
                }
            ]
        },
        {
            "date": "2021-06-03T13:24:56.787113",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "c8a9929e-086d-466f-975c-24dccdc16f78",
                "type": "ORDER"
            },
            "gross": 25,
            "net": 25,
            "fees": []
        },
        {
            "date": "2021-06-03T12:55:32.066130",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "f1685c66-2ae9-40b6-ba0b-fc613567fb43",
                "type": "OFFER"
            },
            "gross": 1.2555,
            "net": 1.0955,
            "fees": [
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.4,
                    "amount": -0.13
                },
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.4,
                    "amount": -0.03
                }
            ]
        },
        {
            "date": "2021-06-03T12:49:44.472909",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "a8fb5ce7-3053-4bd3-af1a-9d5df5caf280",
                "type": "OFFER"
            },
            "gross": 25,
            "net": 22.00,
            "fees": [
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.0,
                    "amount": -2.50
                },
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.0,
                    "amount": -0.50
                }
            ]
        },
        {
            "date": "2021-06-03T12:45:22.301144",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "ead1f572-820c-44b7-b5bd-06ee8ac3f0fd",
                "type": "OFFER"
            },
            "gross": -14.25,
            "net": -14.25,
            "fees": []
        },
        {
            "date": "2021-06-03T12:38:05.753383",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "85149572-dfae-465f-b2d5-dad666c57487",
                "type": "OFFER"
            },
            "gross": -14,
            "net": -14,
            "fees": []
        },
        {
            "date": "2021-06-03T12:22:45.753397",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "71b35b5b-c9c7-44f2-b986-34161f97dce2",
                "type": "OFFER"
            },
            "gross": -5,
            "net": -5,
            "fees": []
        }
    ]
}
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
https://api.arkane.market/user/credits/history
```

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "date": "2021-06-22T19:44:35.896220",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "2367d75e-7e52-45e1-98b7-3ac6ded9e7f1",
                "type": "ORDER"
            },
            "gross": 1.00,
            "net": 1.00,
            "fees": []
        },
        {
            "date": "2021-06-15T20:59:05.609988",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "935870c1-82d5-4f8a-a869-61af6367cda9",
                "type": "ORDER"
            },
            "gross": 100,
            "net": 100,
            "fees": []
        },
        {
            "date": "2021-06-15T20:57:04.647446",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "e95e4717-b720-4560-984b-8847ef37b641",
                "type": "ORDER"
            },
            "gross": 10,
            "net": 10,
            "fees": []
        },
        {
            "date": "2021-06-09T15:14:16.335428",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "a71940cf-18cc-4289-bcad-ddbbfe2b94bf",
                "type": "OFFER"
            },
            "gross": 1,
            "net": 0.88,
            "fees": [
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.0,
                    "amount": -0.02
                },
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.0,
                    "amount": -0.10
                }
            ]
        },
        {
            "date": "2021-06-03T13:24:56.787113",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "DEPOSIT",
            "reference": {
                "id": "c8a9929e-086d-466f-975c-24dccdc16f78",
                "type": "ORDER"
            },
            "gross": 25,
            "net": 25,
            "fees": []
        },
        {
            "date": "2021-06-03T12:55:32.066130",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "f1685c66-2ae9-40b6-ba0b-fc613567fb43",
                "type": "OFFER"
            },
            "gross": 1.2555,
            "net": 1.0955,
            "fees": [
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.4,
                    "amount": -0.13
                },
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.4,
                    "amount": -0.03
                }
            ]
        },
        {
            "date": "2021-06-03T12:49:44.472909",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "SELL",
            "reference": {
                "id": "a8fb5ce7-3053-4bd3-af1a-9d5df5caf280",
                "type": "OFFER"
            },
            "gross": 25,
            "net": 22.00,
            "fees": [
                {
                    "type": "CONTRACT_OWNER_FEE",
                    "percentage": 10.0,
                    "amount": -2.50
                },
                {
                    "type": "MARKET_FEE",
                    "percentage": 2.0,
                    "amount": -0.50
                }
            ]
        },
        {
            "date": "2021-06-03T12:45:22.301144",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "ead1f572-820c-44b7-b5bd-06ee8ac3f0fd",
                "type": "OFFER"
            },
            "gross": -14.25,
            "net": -14.25,
            "fees": []
        },
        {
            "date": "2021-06-03T12:38:05.753383",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "85149572-dfae-465f-b2d5-dad666c57487",
                "type": "OFFER"
            },
            "gross": -14,
            "net": -14,
            "fees": []
        },
        {
            "date": "2021-06-03T12:22:45.753397",
            "userId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "type": "PURCHASE",
            "reference": {
                "id": "71b35b5b-c9c7-44f2-b986-34161f97dce2",
                "type": "OFFER"
            },
            "gross": -5,
            "net": -5,
            "fees": []
        }
    ]
}
```

{% hint style="info" %}
**Gross**: The total amount of the offer\
**Net**: The value that impacts your balance\
**Fees**: The difference between gross and net. Fees that are taken by the market and the collection/contract owner
{% endhint %}

