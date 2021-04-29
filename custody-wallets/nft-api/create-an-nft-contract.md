---
description: >-
  The creation of an NFT contract is the deployment of a new smart contract on a
  specific blockchain. The concept of a contract can be considered as the
  creation of a collection.
---

# Create contract

## Endpoint: POST

```javascript
https://api-business.arkane.network/api/apps/{{application_id}}/contracts
```

## Body

```javascript
{
	"name": "Space Chickens",
	"description":"Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
	"chain" : "MATIC",
	"symbol" : "SPACECHICKS",
  "image" : "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
  "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
  "media" : [
      {"type": "image", "value" : "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"}
  ]
}
```

## Returns

```javascript
{
    "name": "Space Chickens",
    "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
    "confirmed": false,
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

