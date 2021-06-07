---
description: Endpoint to fetch all offers available in the global market
---

# List all offers

{% api-method method="get" host="https://api.arkane.market" path="/offers" %}
{% api-method-summary %}
Get offers
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="type" type="string" required=false %}
Filter all offers by type, '**SALE**' or '**AUCTION**'
{% endapi-method-parameter %}

{% api-method-parameter name="contractAddress" type="string" required=false %}
Filter all offers by contract address
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="array" required=false %}
Filter all offers by status
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

{% hint style="info" %}
The status query parameter is optional, when not provided the endpoint will filter on the [status](../../deep-dive-1/object-reference/status.md) **READY**.
{% endhint %}

## Status

| Description |  |
| :--- | :--- |
| READY | Offer is ready and is live on the market |
| SOLD | Offer has been sold and is no longer active |
| CLOSED | Offer has not been sold and is no longer active |
| NEW | Newly created offer, waiting for Approve tx and signed data |
| INITIATING\_OFFER | Taking an NFT into custody |
| FINALIZING\_OFFER | Moving an NFT out of custody |
| CLOSING\_OFFER | Item was not sold, is being sent back to the user |
| ERROR | Something went wrong... |
| REFUSED | Something went wrong while the item was being sent to the market |

{% page-ref page="../../deep-dive-1/object-reference/status.md" %}

## Example

#### Request

```javascript
//Default filtering applies (status=READY)
https://api.arkane.market/offers

//Filter on status SOLD
https://api.arkane.market/offers?status=SOLD

//Filter on type AUCTION
https://api.arkane.market/offers?type=AUCTION

//Filter on status SOLD and READY
https://api.arkane.market/offers?status=SOLD,READY

//Filter based on contract address (status=READY)
https://api.arkane.market/offers?contractAddress=0x1d9d2d1176e774a6843c2d18d638f2d4ca392e61

//Filter based on contract address and status=SOLD
https://api.arkane.market/offers?status=SOLD&contractAddress=0x1d9d2d1176e774a6843c2d18d638f2d4ca392e61
Respon
```

#### Response

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

