---
description: Endpoint to cancel one of your offers
---

# Cancel an offer

{% api-method method="get" host="https://api.arkane.market" path="/offers/:offerId/cancel" %}
{% api-method-summary %}
Cancel an offer
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="offerId" type="string" required=false %}
ID of the offer to cancel
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
		"id": "ebb1574a-bf3b-43a9-8bf5-ee7b30044f10",
		"nft": {
			"id": "2034",
			"address": "0xA4572039E7925BB175944F0F519Ae603F25e16c2",
			"chain": "MATIC",
			"name": "Arkane Hyperion Front",
			"description": "\"Blockchain Means Business\"\n\nArkane fuels our need for speed, roaring in with a Hyperion based car! Thanks to our friends at Arkane, this car commemorates the launch of the Arkane Market.",
			"imageUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"url": "http://br-stg-rinkeby.altitude-games.com/parts/2034",
			"imagePreviewUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"imageThumbnailUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"attributes": [{
					"type": "property",
					"name": "brand",
					"value": "Arkane"
				},
				{
					"type": "property",
					"name": "model",
					"value": "Hyperion"
				},
				{
					"type": "property",
					"name": "rarity",
					"value": "Rare"
				},
				{
					"type": "property",
					"name": "edition",
					"value": "Special"
				},
				{
					"type": "property",
					"name": "type",
					"value": "Front"
				},
				{
					"type": "property",
					"name": "weight",
					"value": "90"
				},
				{
					"type": "property",
					"name": "power",
					"value": "38"
				},
				{
					"type": "property",
					"name": "durability",
					"value": "53"
				},
				{
					"type": "property",
					"name": "steering",
					"value": "0"
				},
				{
					"type": "property",
					"name": "speed",
					"value": "0"
				}
			],
			"contract": {
				"chain": "MATIC",
				"address": "0xA4572039E7925BB175944F0F519Ae603F25e16c2",
				"count": 0,
				"name": "Battle Racers",
				"description": "Battle Racers is an action-packed blockchain racing game where you design, build, and race NFT cars on arcade-sized tracks. Customize your car in the garage by mixing and matching parts and weapons. Different parts have different stats and skills, contributing to your car’s overall performance. Do you choose speed over handling? Firepower or defense? Create the perfect car to match your playstyle and beat other players to the finish line.",
				"symbol": "BRPART",
				"url": "https://battleracers.io",
				"imageUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/img/arkane.market/BattleRacers-logo.jpeg?raw=true",
				"media": "https://github.com/ArkaneNetwork/content-management/blob/master/img/arkane.market/BattleRacers-banner.jpeg?raw=true"
			}
		},
		"sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"sellerAddress": "0xA5dC4fb59eBCaf00100C00776b45c3E4b58c6B95",
		"startDate": "2021-03-12T15:35:56.669347Z",
		"endDate": "2021-03-12T15:37:53.565075Z",
		"type": "SALE",
		"status": "READY",
		"dataToSign": "ebb1574a-bf3b-43a9-8bf5-ee7b30044f10_0xA5dC4fb59eBCaf00100C00776b45c3E4b58c6B95_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_2034",
		"txInCustody": "0xcf26c1f04c93744a84cae740d14b6712aaf5e2415825b31ee1d4284b8eb7a8b2",
		"createdOn": "2021-03-12T15:35:56.869545Z",
		"createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"modifiedOn": "2021-03-12T15:36:18.483358Z",
		"modifiedBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"signed": true,
		"price": 10000
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
https://api.arkane.market/offers/ebb1574a-bf3b-43a9-8bf5-ee7b30044f10/cancel
```

#### Response

```javascript
{
	"success": true,
	"result": {
		"id": "ebb1574a-bf3b-43a9-8bf5-ee7b30044f10",
		"nft": {
			"id": "2034",
			"address": "0xA4572039E7925BB175944F0F519Ae603F25e16c2",
			"chain": "MATIC",
			"name": "Arkane Hyperion Front",
			"description": "\"Blockchain Means Business\"\n\nArkane fuels our need for speed, roaring in with a Hyperion based car! Thanks to our friends at Arkane, this car commemorates the launch of the Arkane Market.",
			"imageUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"url": "http://br-stg-rinkeby.altitude-games.com/parts/2034",
			"imagePreviewUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"imageThumbnailUrl": "https://s3-ap-southeast-1.amazonaws.com/br-staging.alto.gg/api/images/parts/ArkaneBumper.png",
			"attributes": [{
					"type": "property",
					"name": "brand",
					"value": "Arkane"
				},
				{
					"type": "property",
					"name": "model",
					"value": "Hyperion"
				},
				{
					"type": "property",
					"name": "rarity",
					"value": "Rare"
				},
				{
					"type": "property",
					"name": "edition",
					"value": "Special"
				},
				{
					"type": "property",
					"name": "type",
					"value": "Front"
				},
				{
					"type": "property",
					"name": "weight",
					"value": "90"
				},
				{
					"type": "property",
					"name": "power",
					"value": "38"
				},
				{
					"type": "property",
					"name": "durability",
					"value": "53"
				},
				{
					"type": "property",
					"name": "steering",
					"value": "0"
				},
				{
					"type": "property",
					"name": "speed",
					"value": "0"
				}
			],
			"contract": {
				"chain": "MATIC",
				"address": "0xA4572039E7925BB175944F0F519Ae603F25e16c2",
				"count": 0,
				"name": "Battle Racers",
				"description": "Battle Racers is an action-packed blockchain racing game where you design, build, and race NFT cars on arcade-sized tracks. Customize your car in the garage by mixing and matching parts and weapons. Different parts have different stats and skills, contributing to your car’s overall performance. Do you choose speed over handling? Firepower or defense? Create the perfect car to match your playstyle and beat other players to the finish line.",
				"symbol": "BRPART",
				"url": "https://battleracers.io",
				"imageUrl": "https://github.com/ArkaneNetwork/content-management/blob/master/img/arkane.market/BattleRacers-logo.jpeg?raw=true",
				"media": "https://github.com/ArkaneNetwork/content-management/blob/master/img/arkane.market/BattleRacers-banner.jpeg?raw=true"
			}
		},
		"sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"sellerAddress": "0xA5dC4fb59eBCaf00100C00776b45c3E4b58c6B95",
		"startDate": "2021-03-12T15:35:56.669347Z",
		"endDate": "2021-03-12T15:37:53.565075Z",
		"type": "SALE",
		"status": "READY",
		"dataToSign": "ebb1574a-bf3b-43a9-8bf5-ee7b30044f10_0xA5dC4fb59eBCaf00100C00776b45c3E4b58c6B95_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_2034",
		"txInCustody": "0xcf26c1f04c93744a84cae740d14b6712aaf5e2415825b31ee1d4284b8eb7a8b2",
		"createdOn": "2021-03-12T15:35:56.869545Z",
		"createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"modifiedOn": "2021-03-12T15:36:18.483358Z",
		"modifiedBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"signed": true,
		"price": 10000
	}
}
```

