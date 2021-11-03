---
description: Endpoint to update the price of an existing offer
---

# Update offer price

{% swagger baseUrl="https://api.arkane.market" path="/offers/:offerId/price" method="patch" summary="Update the price of an offer" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="offerId" type="string" required="true" %}
ID of the offer to update
{% endswagger-parameter %}

{% swagger-parameter in="body" name="price" type="string" required="true" %}
The new price of the offer
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the offer information" %}
```json
{
    "success": true,
    "result": {
        "id": "7ae41bf0-fc02-41d3-8e1e-31f5cdf7026f",
        "nft": {
            "id": "452",
            "address": "0xeea32c4db500b21600ed0fa139f7916307bd50c6",
            "chain": "MATIC",
            "name": "Ryu - Street Fighter",
            "description": "Ryu is a fictional Japanese fighting character and the main protagonist of Capcom's Street Fighter series. Having premiered in the first Street Fighter in 1987, Ryu appears as the game's lead character alongside his best friend Ken Masters",
            "imageUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "url": "https://streetfighter.fandom.com/wiki/Ryu",
            "imagePreviewUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "imageThumbnailUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "animationUrls": [
                {
                    "type": "image",
                    "value": "https://i.pinimg.com/originals/90/6b/fe/906bfe4a35cbca6258b04f921223cb27.png"
                }
            ],
            "fungible": false,
            "maxSupply": 10,
            "attributes": [
                {
                    "type": "property",
                    "name": "Power",
                    "value": "9"
                },
                {
                    "type": "property",
                    "name": "Speed",
                    "value": "9"
                },
                {
                    "type": "property",
                    "name": "Ability",
                    "value": "Energy Ball"
                }
            ],
            "contract": {
                "chain": "MATIC",
                "address": "0xeea32c4db500b21600ed0fa139f7916307bd50c6",
                "count": 0,
                "name": "SEED",
                "description": "SEED TEST",
                "symbol": "SEED",
                "url": "seedcms.com",
                "imageUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/settings/SeedCMS-capsule_image_mens-collection.underwear.png",
                "media": [
                    {
                        "type": "unknown",
                        "value": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/settings/SeedCMS-capsule_media_mens-collection.tops.png"
                    }
                ],
                "verified": false,
                "premium": false,
                "categories": []
            }
        },
        "sellerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "sellerAddress": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
        "startDate": "2021-08-09T19:59:50.398634Z",
        "type": "SALE",
        "status": "READY",
        "dataToSign": "7ae41bf0-fc02-41d3-8e1e-31f5cdf7026f_0x39069fb544c7e25122b8a54cd7b982d34d11e470_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_452",
        "txInCustody": "0x054717e82edc70bec5e4aa0d1b712eb35846667a967ea0ac935caf49cfab45a0",
        "createdOn": "2021-08-09T19:59:50.680943Z",
        "createdBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "modifiedOn": "2021-08-09T20:22:23.787778Z",
        "modifiedBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "signed": true,
        "currency": "USDC",
        "price": 9.99
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
The price of a normal sale can always be updated. The price for an auction can only be updated when the auction has **0 bids**.
{% endhint %}

#### **Error codes:**

* **invalid-offer-status**: The offer is not available anymore in the market, either it has been bought or canceled.

## Example

#### Request

```javascript
https://api.arkane.market/offers/18ec506b-1d11-4f94-95f4-e19d89f93da1/price
```

#### Request Body

```java
{
    "price": "9.99"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "7ae41bf0-fc02-41d3-8e1e-31f5cdf7026f",
        "nft": {
            "id": "452",
            "address": "0xeea32c4db500b21600ed0fa139f7916307bd50c6",
            "chain": "MATIC",
            "name": "Ryu - Street Fighter",
            "description": "Ryu is a fictional Japanese fighting character and the main protagonist of Capcom's Street Fighter series. Having premiered in the first Street Fighter in 1987, Ryu appears as the game's lead character alongside his best friend Ken Masters",
            "imageUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "url": "https://streetfighter.fandom.com/wiki/Ryu",
            "imagePreviewUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "imageThumbnailUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/nfts/1628018209831_2650831544-rya.gif",
            "animationUrls": [
                {
                    "type": "image",
                    "value": "https://i.pinimg.com/originals/90/6b/fe/906bfe4a35cbca6258b04f921223cb27.png"
                }
            ],
            "fungible": false,
            "maxSupply": 10,
            "attributes": [
                {
                    "type": "property",
                    "name": "Power",
                    "value": "9"
                },
                {
                    "type": "property",
                    "name": "Speed",
                    "value": "9"
                },
                {
                    "type": "property",
                    "name": "Ability",
                    "value": "Energy Ball"
                }
            ],
            "contract": {
                "chain": "MATIC",
                "address": "0xeea32c4db500b21600ed0fa139f7916307bd50c6",
                "count": 0,
                "name": "SEED",
                "description": "SEED TEST",
                "symbol": "SEED",
                "url": "seedcms.com",
                "imageUrl": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/settings/SeedCMS-capsule_image_mens-collection.underwear.png",
                "media": [
                    {
                        "type": "unknown",
                        "value": "https://storage.googleapis.com/shopify-dev-314109.appspot.com/settings/SeedCMS-capsule_media_mens-collection.tops.png"
                    }
                ],
                "verified": false,
                "premium": false,
                "categories": []
            }
        },
        "sellerId": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "sellerAddress": "0x39069fb544c7e25122b8a54cd7b982d34d11e470",
        "startDate": "2021-08-09T19:59:50.398634Z",
        "type": "SALE",
        "status": "READY",
        "dataToSign": "7ae41bf0-fc02-41d3-8e1e-31f5cdf7026f_0x39069fb544c7e25122b8a54cd7b982d34d11e470_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_452",
        "txInCustody": "0x054717e82edc70bec5e4aa0d1b712eb35846667a967ea0ac935caf49cfab45a0",
        "createdOn": "2021-08-09T19:59:50.680943Z",
        "createdBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "modifiedOn": "2021-08-09T20:22:23.787778Z",
        "modifiedBy": "fd5a4ee7-2cf8-4f33-8978-3649bc447482",
        "signed": true,
        "currency": "USDC",
        "price": 9.99
    }
}
```
