---
description: Create fungible-NFTs based on a predefined NFT template (token-type).
---

# Mint fungible-NFT

## Endpoint: POST

```javascript
https://api-business.arkane.network/api/apps/{{application_id}}/contracts/{{contract_id}}/tokens/fungible/{{token_type_id}}
```

## Body

```javascript
{
  "destinations" : [ "0x39069fB544c7e25122b8A54cD7B982d34d11e470","0x43e6197B707A1bbF6fA8A4b6bfB34f31e82da953" ],
  "amounts": [10,5]
}
```

{% hint style="info" %}
Since **`destinations`** is an array it is possible to provide a list of addresses and by providing a list of **`amounts`** it is possible to mint several NFTs directly to several addresses. As shown in the example above.
{% endhint %}

## Returns

```javascript
[
    {
        "transactionHash": "0x184faec23ba1e2347b9a5fe203bb0e84c5e9cda65c1996e39e6e0d7b1a6634f3",
        "metadata": {
            "name": "Barry The Henn",
            "description": "Barry is Chucks older borther of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
            "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imagePreview": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imageThumbnail": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "backgroundColor": "#eeeeee",
            "background_color": "#eeeeee",
            "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
            "external_url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
            "animationUrls": [],
            "attributes": [
                {
                    "type": "property",
                    "name": "Talent",
                    "value": "Leadership",
                    "traitType": "Talent",
                    "trait_type": "Talent"
                },
                {
                    "type": "property",
                    "name": "Allergic",
                    "value": "Monstonuts",
                    "traitType": "Allergic",
                    "trait_type": "Allergic"
                },
                {
                    "type": "property",
                    "name": "Hobby",
                    "value": "Scouts",
                    "traitType": "Hobby",
                    "trait_type": "Hobby"
                }
            ],
            "contract": {
                "address": "0xd3343d667d8d2c1c9dc6fe36d2b3f6b569e4d08b",
                "name": "Space Chickens",
                "symbol": "SPACECHICKS",
                "image": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "image_url": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                "externalLink": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "external_link": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "external_url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "media": [
                    {
                        "type": "image",
                        "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
                    }
                ],
                "type": "ERC_1155"
            },
            "asset_contract": {
                "address": "0xd3343d667d8d2c1c9dc6fe36d2b3f6b569e4d08b",
                "name": "Space Chickens",
                "symbol": "SPACECHICKS",
                "image": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "image_url": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                "externalLink": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "external_link": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "external_url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "media": [
                    {
                        "type": "image",
                        "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
                    }
                ],
                "type": "ERC_1155"
            },
            "fungible": true
        },
        "destinations": [
            "0x39069fB544c7e25122b8A54cD7B982d34d11e470",
            "0x43e6197B707A1bbF6fA8A4b6bfB34f31e82da953"
        ],
        "tokenIds": [
            52,
            52
        ]
    }
]
```

