---
description: Endpoint to initiate a new offer
---

# Create an offer

{% swagger baseUrl="https://api.arkane.market" path="/offers" method="post" summary="Get offers" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="type" type="string" %}
Type of the offer (SALE / AUCTION)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="nft.tokenId" type="string" %}
TokenID of the NFT
{% endswagger-parameter %}

{% swagger-parameter in="body" name="nft.address" type="string" %}
NFT Contract related to the NFT
{% endswagger-parameter %}

{% swagger-parameter in="body" name="nft.chain" type="string" %}
Blockchain that is hosting the NFT
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sellerAddress" type="string" %}
Address where the NFT is stored
{% endswagger-parameter %}

{% swagger-parameter in="body" name="price" type="string" %}
Price of the offer
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
	"success": true,
	"result": {
		"id": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5",
		"nft": {
			"tokenId": "2",
			"address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
			"chain": "ETHEREUM",
			"name": "Cauliflower Pizza",
			"description": "Awesome cauliflower crust pizza with cured pepperoni. Found on a BBS in the early 80s.",
			"imageUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A",
			"url": "",
			"imagePreviewUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s250",
			"imageThumbnailUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s128",
			"attributes": [{
					"traitType": "topping",
					"value": "cheese",
					"traitCount": 4
				},
				{
					"traitType": "crust",
					"value": "cauliflower",
					"traitCount": 2
				},
				{
					"traitType": "topping",
					"value": "pepperoni",
					"traitCount": 2
				},
				{
					"traitType": "level",
					"value": "7",
					"traitCount": 1
				},
				{
					"traitType": "fuel",
					"value": "3.4",
					"traitCount": 1
				},
				{
					"traitType": "cauliflower_power",
					"value": "80",
					"displayType": "boost_number",
					"traitCount": 1
				},
				{
					"traitType": "bellyfat_increase",
					"value": "3",
					"displayType": "boost_percentage",
					"traitCount": 1
				}
			],
			"contract": {
				"chain": "ETHEREUM",
				"address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
				"count": 0,
				"name": "CryptoPizza Shop",
				"description": "In honor of the dude who paid 10k BTC for two large pizzas in 2010, I'm proud to announce the first ever CryptoPizza Shop! Collect these slices - more to be added soon, but these OG CryptoPizza Slices will go down in history!",
				"symbol": "OSC",
				"imageUrl": "https://rinkeby-storage.opensea.io/0x492aef91afb79efaa508debbed7b3e21069d13e3-1561429292.png"
			}
		},
		"sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"sellerAddress": "0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690",
		"startDate": "2020-10-21T14:46:09.252659Z",
		"endDate": "2020-10-31T14:46:09.252674Z",
		"type": "SALE",
		"status": "NEW",
		"dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
		"createdOn": "2020-10-21T14:46:09.305261Z",
		"createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"price": 25
	}
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
This endpoint will create a new offer with the [status](../../deep-dive-1/object-reference/status.md) **NEW**. Once a new offer is created it needs to be updated **first** with [Update offer: TxApprove](update-offer-txapprove/), follow by [Update offer: Signature](update-offer-signature.md) before it can move to the state **READY** and become live on the market.
{% endhint %}

{% hint style="warning" %}
**Note: **The order is important. First the TxApprove, then the Signature.&#x20;
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.market/offers
```

#### Request Body

```javascript
{
    "type": "SALE",
    "nft": {
        "tokenId": "2",
        "address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
        "chain": "ETHEREUM"
    },
    "sellerAddress": "0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690",
    "price": 25
}
```

#### Response

```javascript
{
	"success": true,
	"result": {
		"id": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5",
		"nft": {
			"tokenId": "2",
			"address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
			"chain": "ETHEREUM",
			"name": "Cauliflower Pizza",
			"description": "Awesome cauliflower crust pizza with cured pepperoni. Found on a BBS in the early 80s.",
			"imageUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A",
			"url": "",
			"imagePreviewUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s250",
			"imageThumbnailUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s128",
			"attributes": [{
					"traitType": "topping",
					"value": "cheese",
					"traitCount": 4
				},
				{
					"traitType": "crust",
					"value": "cauliflower",
					"traitCount": 2
				},
				{
					"traitType": "topping",
					"value": "pepperoni",
					"traitCount": 2
				},
				{
					"traitType": "level",
					"value": "7",
					"traitCount": 1
				},
				{
					"traitType": "fuel",
					"value": "3.4",
					"traitCount": 1
				},
				{
					"traitType": "cauliflower_power",
					"value": "80",
					"displayType": "boost_number",
					"traitCount": 1
				},
				{
					"traitType": "bellyfat_increase",
					"value": "3",
					"displayType": "boost_percentage",
					"traitCount": 1
				}
			],
			"contract": {
				"chain": "ETHEREUM",
				"address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
				"count": 0,
				"name": "CryptoPizza Shop",
				"description": "In honor of the dude who paid 10k BTC for two large pizzas in 2010, I'm proud to announce the first ever CryptoPizza Shop! Collect these slices - more to be added soon, but these OG CryptoPizza Slices will go down in history!",
				"symbol": "OSC",
				"imageUrl": "https://rinkeby-storage.opensea.io/0x492aef91afb79efaa508debbed7b3e21069d13e3-1561429292.png"
			}
		},
		"sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"sellerAddress": "0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690",
		"startDate": "2020-10-21T14:46:09.252659Z",
		"type": "SALE",
		"status": "NEW",
		"dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
		"createdOn": "2020-10-21T14:46:09.305261Z",
		"createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
		"price": 25
	}
}
```
