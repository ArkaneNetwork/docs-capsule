---
description: Endpoint to pass the signature of the end-user to the market
---

# Update offer: Signature

The last step in the offer creation is getting the signature of the end-user, proving to the market that the end-user agrees with selling the NFT and allow the market to take the NFT into custody.

This is done by asking the end-user to sign a piece of data. The data that is required to sign can be found in the details of the offer, more specifically the `dataToSign` attribute. To get the details of an offer please take a look at [Retrieve an offer](retrieve-an-offer.md).

{% page-ref page="retrieve-an-offer.md" %}

{% api-method method="patch" host="https://api.arkane.market" path="/offers/:offerId/signature" %}
{% api-method-summary %}
Update offer: Signature
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="offerId" type="string" required=true %}
ID of the offer that needs the update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="signature" type="string" required=true %}
Signature of the signed data of the `dataToSign` attribute.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
            "attributes": [
                {
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
        "status": "INITIATING_OFFER",
        "dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
        "createdOn": "2020-10-21T14:46:09.305261Z",
        "createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "price": 25
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
After updating the offer with the signature the status of the offer will transition from **NEW** to **INITIATING\_OFFER**, meaning the NFT will be taken into custody. If that was successful the status will be updated to **READY**. Meaning the offer was successfully created and is live on the market.
{% endhint %}

{% hint style="warning" %}
Note this step assumes you've already completed [Update offer: TxApprove](update-offer-txapprove/). 
{% endhint %}

## Example

#### Request

```javascript
https://api-qa.arkane.market/offers/b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5/signature
```

#### Request Body

```javascript
{
    "signature": "0x1893702698b9daa97313817e2b58dbaeabb9de1cfa3fede14ec00e9dbbd899835dd184fa6f63a2eb67beea34b8ad698fbb7bd887bcc1c88539df43963779fde51b"
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
            "attributes": [
                {
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
        "status": "INITIATING_OFFER",
        "dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
        "createdOn": "2020-10-21T14:46:09.305261Z",
        "createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "price": 25
    }
}
```

