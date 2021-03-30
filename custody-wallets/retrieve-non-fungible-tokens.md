---
description: How to retrieve non-fungible tokens for a wallet.
---

# Retrieve non-fungible tokens

NFTs can be queried either by wallet ID or by wallet address, if required multiple NFT contract addresses can be passed as a query parameter to act as a filter. 

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/<walletId>/nonfungibles" %}
{% api-method-summary %}
Get NFTs by wallet ID
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletId" type="string" required=true %}
ID of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="contract-addresses" type="string" required=false %}
When set, the result will only contain tokens of these NFT contract addresses. Multiple values can be set.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "description": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
            "url": null,
            "backgroundColor": null,
            "imageUrl": null,
            "imagePreviewUrl": null,
            "imageThumbnailUrl": null,
            "animationUrl": null,
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men",
                "description": null,
                "address": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155"
            },
            "attributes": null
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.arkane.network" path="/api/wallets/MATIC/<walletAddress>/nonfungibles" %}
{% api-method-summary %}
Get NFTs by wallet address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="walletAddress" type="string" required=true %}
Blockchain address of the wallet
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="contract-addresses" type="string" required=false %}
When set, the result will only contain tokens of these NFT contract addresses. Multiple values can be set.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": [
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "description": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
            "url": null,
            "backgroundColor": null,
            "imageUrl": null,
            "imagePreviewUrl": null,
            "imageThumbnailUrl": null,
            "animationUrl": null,
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men",
                "description": null,
                "address": "0xd38fa822553dd606618ad25fb5f6d18aefcbac1b",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155"
            },
            "attributes": null
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": [
        {
            "id": "203",
            "name": "Chuck",
            "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
            "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
            "backgroundColor": null,
            "imageUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imagePreviewUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imageThumbnailUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": 1000,
            "contract": {
                "name": "Space Chickens",
                "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                "address": "0x753d61c8a7b7a6e8adb6c759eb49190ef6a24401",
                "symbol": "SPACECHICKS",
                "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "media": [
                    {
                        "type": "unknown",
                        "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
                    }
                ],
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": [
                {
                    "type": "property",
                    "name": "Talent",
                    "value": "Leadership",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "property",
                    "name": "Allergic",
                    "value": "Monstonuts",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "property",
                    "name": "Hobby",
                    "value": "Scouts",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "stat",
                    "name": "Cool",
                    "value": "9",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Daring",
                    "value": "8",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Noise",
                    "value": "8",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Age",
                    "value": "3",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "boost",
                    "name": "Crafting",
                    "value": "+5",
                    "displayType": "boost_number",
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "boost",
                    "name": "Leadership",
                    "value": "+10",
                    "displayType": "boost_number",
                    "traitCount": null,
                    "maxValue": null
                }
            ]
        },
        {
            "id": "57896044618658097711785492504343953927315557066662158946655541218820101242887",
            "name": "Example Type: Hulk",
            "description": "Robert Bruce Banner a.k.a The Incredible Hulk",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imagePreviewUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imageThumbnailUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men Heroes",
                "description": "The X-Men are a team of mutant superheroes in the Marvel Universe. he basic concept of the X-Men is that under a cloud of increasing anti-mutant sentiment, Professor Xavier created a haven at his Westchester mansion to train young mutants to use their powers for the benefit of humanity, and to prove mutants can be heroes",
                "address": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        },
        {
            "id": "57896044618658097711785492504343953927315557066662158946655541218820101242883",
            "name": "Example Type: Hulk",
            "description": "Robert Bruce Banner a.k.a The Incredible Hulk",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imagePreviewUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imageThumbnailUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men Heroes",
                "description": "The X-Men are a team of mutant superheroes in the Marvel Universe. he basic concept of the X-Men is that under a cloud of increasing anti-mutant sentiment, Professor Xavier created a haven at his Westchester mansion to train young mutants to use their powers for the benefit of humanity, and to prove mutants can be heroes",
                "address": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        },
        {
            "id": "57896044618658097711785492504343953927315557066662158946655541218820101242884",
            "name": "Example Type: Hulk",
            "description": "Robert Bruce Banner a.k.a The Incredible Hulk",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imagePreviewUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "imageThumbnailUrl": "https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "X-Men Heroes",
                "description": "The X-Men are a team of mutant superheroes in the Marvel Universe. he basic concept of the X-Men is that under a cloud of increasing anti-mutant sentiment, Professor Xavier created a haven at his Westchester mansion to train young mutants to use their powers for the benefit of humanity, and to prove mutants can be heroes",
                "address": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
                "symbol": "X-MEN",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        },
        {
            "id": "2",
            "name": "Gaimin Chuck",
            "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
            "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
            "backgroundColor": null,
            "imageUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imagePreviewUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "imageThumbnailUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
            "animationUrl": "https://i.pinimg.com/originals/6a/34/9e/6a349ef34e90c467cf7bd5804de6b095.gif",
            "animationUrls": [
                {
                    "type": "unknown",
                    "value": "https://i.pinimg.com/originals/6a/34/9e/6a349ef34e90c467cf7bd5804de6b095.gif"
                }
            ],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "Gaimin Chickens",
                "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                "address": "0x4ddbb33ca06363ce79e2a42ea2df70436efb6ec9",
                "symbol": "SPACECHICKS",
                "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                "media": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg",
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": [
                {
                    "type": "property",
                    "name": "Talent",
                    "value": "Leadership",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "property",
                    "name": "Allergic",
                    "value": "Monstonuts",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "property",
                    "name": "Hobby",
                    "value": "Scouts",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "stat",
                    "name": "Cool",
                    "value": "9",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Daring",
                    "value": "8",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Noise",
                    "value": "8",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": 10
                },
                {
                    "type": "stat",
                    "name": "Age",
                    "value": "3",
                    "displayType": "number",
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "boost",
                    "name": "Crafting",
                    "value": "+5",
                    "displayType": "boost_number",
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "boost",
                    "name": "Leadership",
                    "value": "+10",
                    "displayType": "boost_number",
                    "traitCount": null,
                    "maxValue": null
                }
            ]
        },
        {
            "id": "1",
            "name": "Hopeful sunset",
            "description": "Pirates 2048 - Survivor art",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://gateway.pinata.cloud/ipfs/QmTbXqqBdLQvX3KMGX2cA9jA7nbi5oJq1Xjy1ZRE29CY6T",
            "imagePreviewUrl": "https://gateway.pinata.cloud/ipfs/QmTbXqqBdLQvX3KMGX2cA9jA7nbi5oJq1Xjy1ZRE29CY6T",
            "imageThumbnailUrl": "https://gateway.pinata.cloud/ipfs/QmTbXqqBdLQvX3KMGX2cA9jA7nbi5oJq1Xjy1ZRE29CY6T",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "Pirates 2048 Art",
                "description": null,
                "address": "0x7b03246eb190627a3549d44e96ea606e17dfe758",
                "symbol": "48ART",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_721",
                "verified": false
            },
            "attributes": [
                {
                    "type": "property",
                    "name": "Signature",
                    "value": "MS",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                },
                {
                    "type": "property",
                    "name": "Origin",
                    "value": "Sea bottle",
                    "displayType": null,
                    "traitCount": null,
                    "maxValue": null
                }
            ]
        },
        {
            "id": "57896044618658097711785492504343953935482333872764682069776531797182538317826",
            "name": "Lucky Gold Horseshoe",
            "description": "",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "imagePreviewUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "imageThumbnailUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "CryptoPick",
                "description": "A test inventory (staging) for CryptoPick skins.",
                "address": "0x8b7647ee5a8ef0fc93a2876835faf7be3fbf2085",
                "symbol": "CP",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        },
        {
            "id": "57896044618658097711785492504343953935482333872764682069776531797182538317828",
            "name": "Lucky Gold Horseshoe",
            "description": "",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "imagePreviewUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "imageThumbnailUrl": "https://staging.cryptopick.net/images/avatars/parts/claws/lucky-golden-horseshoe.svg",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "CryptoPick",
                "description": "A test inventory (staging) for CryptoPick skins.",
                "address": "0x8b7647ee5a8ef0fc93a2876835faf7be3fbf2085",
                "symbol": "CP",
                "url": null,
                "imageUrl": null,
                "media": null,
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        },
        {
            "id": "57896044618658097711785492504343953926975274699741220483192166611388333031425",
            "name": "Silkie",
            "description": "The Silkie (sometimes spelled Silky) is a breed of chicken named for its atypically fluffy plumage, which is said to feel like silk and satin. The breed has several other unusual qualities, such as black skin and bones, blue earlobes, and five toes on each foot, whereas most chickens only have four. They are often exhibited in poultry shows, and appear in various colors. In addition to their distinctive physical characteristics, Silkies are well known for their calm, friendly temperament. It is among the most docile of poultry. Hens are also exceptionally broody, and care for young well. Though they are fair layers themselves, laying only about three eggs a week, they are commonly used to hatch eggs from other breeds and bird species due to their broody nature. Silkie chickens are very easy to keep as pets. They are suitable for children, but like any pet, should be handled with care.",
            "url": null,
            "backgroundColor": null,
            "imageUrl": "https://upload.wikimedia.org/wikipedia/commons/3/36/A_fuzzy_baby_chicken_and_its_mom.jpg",
            "imagePreviewUrl": "https://upload.wikimedia.org/wikipedia/commons/3/36/A_fuzzy_baby_chicken_and_its_mom.jpg",
            "imageThumbnailUrl": "https://upload.wikimedia.org/wikipedia/commons/3/36/A_fuzzy_baby_chicken_and_its_mom.jpg",
            "animationUrl": null,
            "animationUrls": [],
            "fungible": false,
            "maxSupply": null,
            "contract": {
                "name": "CryptoChickies",
                "description": "Chickens on a blockchain? Now I've seen everything",
                "address": "0x5cd477d3ae9883ea41dd0b0ece1e22718b948289",
                "symbol": "ARKN",
                "url": null,
                "imageUrl": null,
                "media": [],
                "type": "ERC_1155",
                "verified": false
            },
            "attributes": []
        }
    ]
}
```

