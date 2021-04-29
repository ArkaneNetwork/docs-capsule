---
description: How to retrieve the information of an NFT contract
---

# Retrieve NFT Contract

## Endpoint: GET

```javascript
https://api-business.arkane.network/api/apps/{{application_id}}/contracts/{{contract_id}}
```

## Example

```javascript
https://api-business.arkane.network/api/apps/0aaa40b2-590f-4a14-b4a2-5d30c7b2b626/contracts/203
```

## Returns

```javascript
{
    "name": "Space Chickens",
    "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
    "confirmed": true,
    "address": "0xd3343d667d8d2c1c9dc6fe36d2b3f6b569e4d08b",
    "id": 203,
    "secretType": "MATIC",
    "symbol": "SPACECHICKS",
    "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
    "image": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
    "media": [
        {
            "type": "image",
            "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
        }
    ],
    "transactionHash": "0x959fdb61ab62354f780e7fce22c650f51e1d71a80f055062559719723858e3f4"
}
```

