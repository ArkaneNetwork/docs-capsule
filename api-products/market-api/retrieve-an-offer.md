---
description: Endpoint to fetch one specific offer
---

# Retrieve an offer

{% api-method method="get" host="https://api.arkane.market" path="/offers/:offerId" %}
{% api-method-summary %}
Get specific offer
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="offerId" type="string" required=true %}
ID of the offer to fetch
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "id": "476477b1-c4bb-49c2-a390-bcfd51da80b3",
            "nft": {
                "id": "51",
                "address": "0x7940e73832403de364568ce406bd4792097b6594",
                "chain": "MATIC",
                "name": "Chuck",
                "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
                "imageUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "imagePreviewUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "imageThumbnailUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "animationUrls": [],
                "fungible": false,
                "maxSupply": 1,
                "attributes": [
                    {
                        "type": "property",
                        "name": "Talent",
                        "value": "Leadership"
                    },
                    {
                        "type": "stat",
                        "name": "Noise",
                        "value": "8",
                        "displayType": "number",
                        "maxValue": 10
                    },
                    {
                        "type": "boost",
                        "name": "Leadership",
                        "value": "+10",
                        "displayType": "boost_number"
                    }
                ],
                "contract": {
                    "chain": "MATIC",
                    "address": "0x7940e73832403de364568ce406bd4792097b6594",
                    "count": 0,
                    "name": "Space Chickens",
                    "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                    "symbol": "SPACECHICKS",
                    "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                    "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                    "media": [
                        {
                            "type": "unknown",
                            "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
                        }
                    ],
                    "verified": false,
                    "premium": false,
                    "categories": []
                }
            },
            "sellerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "sellerAddress": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
            "startDate": "2021-02-01T20:08:55.815300Z",
            "type": "SALE",
            "status": "SOLD",
            "dataToSign": "476477b1-c4bb-49c2-a390-bcfd51da80b3_0x39069fB544c7e25122b8A54cD7B982d34d11e470_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_51",
            "txApprove": "0x7bd97c5ec699297c78a24ab1788f36059fd8b4dab68961b839743b8cc383ac19",
            "txInCustody": "0x8f37687630cb0321a7c411a445f7bc45ada1090ea74eb4f6dbdd6d9feb787eb1",
            "txOutOfCustody": "0x7089da6b0e124d117e60b4dab8300f3524c98da4538ad5e6f15cc327c5ad3c3a",
            "createdOn": "2021-02-01T20:08:55.817546Z",
            "createdBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "modifiedOn": "2021-02-02T16:14:35.191498Z",
            "modifiedBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "signed": true,
            "currency": "USDC",
            "price": 15.99,
            "buyerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "soldOn": "2021-02-02T16:14:26.076765Z"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

```javascript
https://api.arkane.market/offers/ac7e55a3-31eb-4546-9a7f-36b2f8d4523d
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "476477b1-c4bb-49c2-a390-bcfd51da80b3",
            "nft": {
                "id": "51",
                "address": "0x7940e73832403de364568ce406bd4792097b6594",
                "chain": "MATIC",
                "name": "Chuck",
                "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
                "imageUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                "imagePreviewUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "imageThumbnailUrl": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg/revision/latest/scale-to-width-down/340?cb=20200105162539",
                "animationUrls": [],
                "fungible": false,
                "maxSupply": 1,
                "attributes": [
                    {
                        "type": "property",
                        "name": "Talent",
                        "value": "Leadership"
                    },
                    {
                        "type": "stat",
                        "name": "Noise",
                        "value": "8",
                        "displayType": "number",
                        "maxValue": 10
                    },
                    {
                        "type": "boost",
                        "name": "Leadership",
                        "value": "+10",
                        "displayType": "boost_number"
                    }
                ],
                "contract": {
                    "chain": "MATIC",
                    "address": "0x7940e73832403de364568ce406bd4792097b6594",
                    "count": 0,
                    "name": "Space Chickens",
                    "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
                    "symbol": "SPACECHICKS",
                    "url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
                    "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
                    "media": [
                        {
                            "type": "unknown",
                            "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
                        }
                    ],
                    "verified": false,
                    "premium": false,
                    "categories": []
                }
            },
            "sellerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "sellerAddress": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
            "startDate": "2021-02-01T20:08:55.815300Z",
            "type": "SALE",
            "status": "SOLD",
            "dataToSign": "476477b1-c4bb-49c2-a390-bcfd51da80b3_0x39069fB544c7e25122b8A54cD7B982d34d11e470_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_51",
            "txApprove": "0x7bd97c5ec699297c78a24ab1788f36059fd8b4dab68961b839743b8cc383ac19",
            "txInCustody": "0x8f37687630cb0321a7c411a445f7bc45ada1090ea74eb4f6dbdd6d9feb787eb1",
            "txOutOfCustody": "0x7089da6b0e124d117e60b4dab8300f3524c98da4538ad5e6f15cc327c5ad3c3a",
            "createdOn": "2021-02-01T20:08:55.817546Z",
            "createdBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "modifiedOn": "2021-02-02T16:14:35.191498Z",
            "modifiedBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "signed": true,
            "currency": "USDC",
            "price": 15.99,
            "buyerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
            "soldOn": "2021-02-02T16:14:26.076765Z"
    }
}
```

