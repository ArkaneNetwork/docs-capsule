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
{% api-method-parameter name="offerId" type="string" required=false %}
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
	"result": [{
			"id": "fb9df783-2fc7-42c2-836e-d1ef882c3519",
			"nft": {
				"id": "56",
				"address": "0xab858ae48772aee79a9c2e54c760e33aa397c73a",
				"chain": "MATIC",
				"name": "Chuck",
				"description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
				"imageUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Solomone%20-%20Dzelshavi.gif?raw=true",
				"url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
				"imagePreviewUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Solomone%20-%20Dzelshavi.gif?raw=true",
				"imageThumbnailUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Solomone%20-%20Dzelshavi.gif?raw=true",
				"animationUrls": [{
						"type": "youtube",
						"value": "https://www.youtube.com/watch?v=3gSmS1BgbOU"
					},
					{
						"type": "unknown",
						"value": "https://i.pinimg.com/originals/6a/34/9e/6a349ef34e90c467cf7bd5804de6b095.gif"
					}
				],
				"fungible": false,
				"attributes": [{
						"type": "property",
						"name": "Talent",
						"value": "Leadership"
					},
					{
						"type": "property",
						"name": "Allergic",
						"value": "Monstonuts"
					},
					{
						"type": "property",
						"name": "Hobby",
						"value": "Scouts"
					},
					{
						"type": "stat",
						"name": "Cool",
						"value": "9",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Daring",
						"value": "8",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Noise",
						"value": "8",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Age",
						"value": "3",
						"displayType": "number"
					},
					{
						"type": "boost",
						"name": "Crafting",
						"value": "+5",
						"displayType": "boost_number"
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
					"address": "0xab858ae48772aee79a9c2e54c760e33aa397c73a",
					"count": 0,
					"name": "Space Chickens",
					"description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
					"symbol": "SPACECHICKS",
					"url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
					"imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg/revision/latest?cb=20181227162543",
					"media": [{
						"type": "unknown",
						"value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
					}],
					"verified": false,
					"premium": false,
					"categories": []
				}
			},
			"sellerId": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"sellerAddress": "0xc58433a1db532c8b9725bea2f2fb920c12b10e59",
			"startDate": "2021-05-12T11:25:21.188647Z",
			"type": "SALE",
			"status": "READY",
			"dataToSign": "fb9df783-2fc7-42c2-836e-d1ef882c3519_0xC58433a1Db532c8B9725bea2f2Fb920c12b10E59_0x72C38DFF5Deb65F019f547170dEDd946104d573D_56",
			"txInCustody": "0x08f77e9cfdf2b9cc8ccc19fd3775beccb3aac4cadf9b1f7df15e25adc9eda1eb",
			"createdOn": "2021-05-12T11:25:21.190660Z",
			"createdBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"modifiedOn": "2021-05-12T11:26:08.577920Z",
			"modifiedBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"signed": true,
			"price": 1000000
		},
		{
			"id": "6deefa7e-68f1-4f11-ad38-dc2b0b844a8a",
			"nft": {
				"id": "52",
				"address": "0xab858ae48772aee79a9c2e54c760e33aa397c73a",
				"chain": "MATIC",
				"name": "Chuck",
				"description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
				"imageUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Barla%20-%20Light.gif?raw=true",
				"url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
				"imagePreviewUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Barla%20-%20Light.gif?raw=true",
				"imageThumbnailUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/market/promo/img/Barla%20-%20Light.gif?raw=true",
				"animationUrls": [{
						"type": "youtube",
						"value": "https://www.youtube.com/watch?v=3gSmS1BgbOU"
					},
					{
						"type": "unknown",
						"value": "https://i.pinimg.com/originals/6a/34/9e/6a349ef34e90c467cf7bd5804de6b095.gif"
					}
				],
				"fungible": false,
				"attributes": [{
						"type": "property",
						"name": "Talent",
						"value": "Leadership"
					},
					{
						"type": "property",
						"name": "Allergic",
						"value": "Monstonuts"
					},
					{
						"type": "property",
						"name": "Hobby",
						"value": "Scouts"
					},
					{
						"type": "stat",
						"name": "Cool",
						"value": "9",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Daring",
						"value": "8",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Noise",
						"value": "8",
						"displayType": "number",
						"maxValue": 10
					},
					{
						"type": "stat",
						"name": "Age",
						"value": "3",
						"displayType": "number"
					},
					{
						"type": "boost",
						"name": "Crafting",
						"value": "+5",
						"displayType": "boost_number"
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
					"address": "0xab858ae48772aee79a9c2e54c760e33aa397c73a",
					"count": 0,
					"name": "Space Chickens",
					"description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
					"symbol": "SPACECHICKS",
					"url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
					"imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg/revision/latest?cb=20181227162543",
					"media": [{
						"type": "unknown",
						"value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
					}],
					"verified": false,
					"premium": false,
					"categories": []
				}
			},
			"sellerId": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"sellerAddress": "0xc58433a1db532c8b9725bea2f2fb920c12b10e59",
			"startDate": "2021-05-12T11:24:20.116932Z",
			"type": "SALE",
			"status": "READY",
			"dataToSign": "6deefa7e-68f1-4f11-ad38-dc2b0b844a8a_0xC58433a1Db532c8B9725bea2f2Fb920c12b10E59_0x72C38DFF5Deb65F019f547170dEDd946104d573D_52",
			"txInCustody": "0xc5190cc31928b380b21a64d932aaf1965f97da23092ef438b3965490db32d49c",
			"createdOn": "2021-05-12T11:24:20.119762Z",
			"createdBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"modifiedOn": "2021-05-12T11:25:13.003391Z",
			"modifiedBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
			"signed": true,
			"price": 1000000
		},
		...
	]
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
        "id": "ac7e55a3-31eb-4546-9a7f-36b2f8d4523d",
        "nft": {
            "id": "57896044618658097711785492504343953927655839433583097410118915826251869454339",
            "address": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
            "chain": "MATIC",
            "name": "Gambit",
            "description": "Gambit belongs to a subspecies of humans called mutants, who are born with superhuman abilities. Gambit has the ability to mentally create, control, and manipulate pure kinetic energy to his desire. He is also incredibly knowledgeable and skilled in card throwing, hand-to-hand combat, and the use of a bō staff. Gambit is known to charge playing cards and other objects with kinetic energy, using them as explosive projectiles.",
            "imageUrl": "https://vignette.wikia.nocookie.net/ultimateallstars/images/3/34/Gambit_Portrait_Art.png",
            "imagePreviewUrl": "https://vignette.wikia.nocookie.net/ultimateallstars/images/3/34/Gambit_Portrait_Art.png",
            "imageThumbnailUrl": "https://vignette.wikia.nocookie.net/ultimateallstars/images/3/34/Gambit_Portrait_Art.png",
            "animationUrls": [],
            "fungible": false,
            "attributes": [],
            "contract": {
                "chain": "MATIC",
                "address": "0x563966a99550b1a7d1d917e2da28c6c59999f19f",
                "count": 0,
                "name": "X-Men Heroes",
                "description": "The X-Men are a team of mutant superheroes in the Marvel Universe. he basic concept of the X-Men is that under a cloud of increasing anti-mutant sentiment, Professor Xavier created a haven at his Westchester mansion to train young mutants to use their powers for the benefit of humanity, and to prove mutants can be heroes",
                "symbol": "X-MEN",
                "media": [],
                "verified": false,
                "premium": false,
                "categories": []
            }
        },
        "sellerId": "4917b6fa-2657-4bdd-b8e8-fa5dd8bd4057",
        "sellerAddress": "0xbb5b5fdc6d627d1991a7a3fd543c79af5cd537ae",
        "startDate": "2021-05-21T12:26:06.311843Z",
        "endDate": "2021-05-21T12:52:09.874373Z",
        "type": "SALE",
        "status": "CLOSED",
        "dataToSign": "ac7e55a3-31eb-4546-9a7f-36b2f8d4523d_0xbb5b5fdc6d627d1991a7a3fd543c79af5cd537ae_0x72C38DFF5Deb65F019f547170dEDd946104d573D_57896044618658097711785492504343953927655839433583097410118915826251869454339",
        "txApprove": "0x840bc5afecdaa66fb262e75d09421b0081518cb3ea499a55c4dac689dd71aa7d",
        "txInCustody": "0xed3f4af325fad0aaf882feb6e9c33db706b69eb7df87ce95875437db86f15e81",
        "txOutOfCustody": "0xf88d83146a26766e23f526b9752cb63525718f68bd6182f623a4f5bf3b7e9348",
        "createdOn": "2021-05-21T12:26:06.316110Z",
        "createdBy": "4917b6fa-2657-4bdd-b8e8-fa5dd8bd4057",
        "modifiedOn": "2021-05-21T12:52:44.546229Z",
        "modifiedBy": "4917b6fa-2657-4bdd-b8e8-fa5dd8bd4057",
        "signed": true,
        "price": 666
    }
}
```

