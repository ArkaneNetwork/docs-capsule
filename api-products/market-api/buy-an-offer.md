---
description: Endpoint to buy a certain offer
---

# Buy an offer

{% swagger baseUrl="https://api.arkane.market" path="/offers/:offerId/buy" method="post" summary="Buy an offer" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="offerId" type="string" %}
ID of the offer to cancel
{% endswagger-parameter %}

{% swagger-parameter in="body" name="externalUserId" type="string" %}
String to identify the end-user, the buyer.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletAddress" type="string" %}
Address of the buyer, NFT will be sent to that address
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "success": true,
    "result": {
        "id": "18ec506b-1d11-4f94-95f4-e19d89f93da1",
        "nft": {
            "tokenId": "57896044618658097711785492504343953927655839433583097410118915826251869454343",
            "address": "0x77d2372fabe8ad47e342a65944a87991adcf2c8a",
            "chain": "MATIC",
            "name": "B-52 Stratofortress",
            "description": "The B-52, also called Stratofortress, is a U.S. long-range heavy bomber designed by the Boeing Company in 1948, first flown in 1952, and first delivered for military service in 1955. Though originally intended to be an atomic-bomb carrier capable of reaching the Soviet Union, it has proved adaptable to a number of missions, and some B-52s are expected to remain in service well into the 21st century. The B-52 has a wingspan of 185 feet (56 meters) and a length of 160 feet 10.9 inches (49 meters). It is powered by eight jet engines mounted under the wings in four twin pods. The plane’s maximum speed at 55,000 feet (17,000 meters) is Mach 0.9 (595 miles per hour, or 960 km/hr); at only a few hundred feet above the ground, it can fly at Mach 0.5 (375 miles per hour, or 600 km/hr). It originally carried a crew of six, its sole defensive armament being a remotely controlled gun turret in the tail. In 1991 the gun was eliminated and the crew reduced to five.",
            "imageUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "backgroundColor": "#c8e2eb",
            "imagePreviewUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "imageThumbnailUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "contract": {
                "chain": "MATIC",
                "address": "0x77d2372fabe8ad47e342a65944a87991adcf2c8a",
                "count": 0,
                "name": "Warplanes",
                "description": "The newest warplanes test contract"
            }
        },
        "sellerId": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
        "sellerAddress": "0x5F81D2867996baFee01e109fBcC8e3AD2Edf044E",
        "startDate": "2020-10-26T13:33:15.908141Z",
        "endDate": "2020-11-05T13:33:15.908158Z",
        "type": "SALE",
        "status": "FINALIZING_OFFER",
        "dataToSign": "18ec506b-1d11-4f94-95f4-e19d89f93da1_0x5F81D2867996baFee01e109fBcC8e3AD2Edf044E_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_57896044618658097711785492504343953927655839433583097410118915826251869454343",
        "txInCustody": "0x4f7fd89195bcd4f84b35c873cbf5a013df948fa1fd71f89d9d0f3c9f1d500c20",
        "txOutOfCustody": "0x2e6b7e9923fb9348ef6ce55f472668c71b193b46468e79879639230483d525af",
        "createdOn": "2020-10-26T13:33:15.943301Z",
        "createdBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
        "price": 200,
        "buyerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "buyerWalletAddress": "0x8D6331D6C5ba3306961F0b4Ea13ff13aa43560b9",
        "externalBuyerId": "yourUserIdentifier",
        "soldOn": "2020-11-05T09:28:48.569562Z"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
When an offer is bought, the state of the offer transitions from **READY** to **FINALIZNIG\_OFFER**, once the NFT is successfully transferred to the buyer's wallet the status gets updated one last time to **SOLD**.

Learn more about the different [states](../../deep-dive-1/object-reference/status.md).
{% endhint %}

{% hint style="warning" %}
If the **`walletAddress`** is invalid, the NFT will be sent to the email address of the buyer. In an API solution that would mean the email address of the Client.&#x20;
{% endhint %}

## Example

#### Request

```javascript
https://api.arkane.market/offers/18ec506b-1d11-4f94-95f4-e19d89f93da1/buy
```

#### Request Body

```java
{
	"externalUserId": "yourUserIdentifier",
  "walletAddress": "0xF70e8Cedc8C0e4777df5504c5aA1e317A29388B0"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "18ec506b-1d11-4f94-95f4-e19d89f93da1",
        "nft": {
            "tokenId": "57896044618658097711785492504343953927655839433583097410118915826251869454343",
            "address": "0x77d2372fabe8ad47e342a65944a87991adcf2c8a",
            "chain": "MATIC",
            "name": "B-52 Stratofortress",
            "description": "The B-52, also called Stratofortress, is a U.S. long-range heavy bomber designed by the Boeing Company in 1948, first flown in 1952, and first delivered for military service in 1955. Though originally intended to be an atomic-bomb carrier capable of reaching the Soviet Union, it has proved adaptable to a number of missions, and some B-52s are expected to remain in service well into the 21st century. The B-52 has a wingspan of 185 feet (56 meters) and a length of 160 feet 10.9 inches (49 meters). It is powered by eight jet engines mounted under the wings in four twin pods. The plane’s maximum speed at 55,000 feet (17,000 meters) is Mach 0.9 (595 miles per hour, or 960 km/hr); at only a few hundred feet above the ground, it can fly at Mach 0.5 (375 miles per hour, or 600 km/hr). It originally carried a crew of six, its sole defensive armament being a remotely controlled gun turret in the tail. In 1991 the gun was eliminated and the crew reduced to five.",
            "imageUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "backgroundColor": "#c8e2eb",
            "imagePreviewUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "imageThumbnailUrl": "https://cdn.britannica.com/s:800x1000/49/106949-131-0783F166/US-Air-Force-cruise-missiles-attack-B-52G.jpg",
            "contract": {
                "chain": "MATIC",
                "address": "0x77d2372fabe8ad47e342a65944a87991adcf2c8a",
                "count": 0,
                "name": "Warplanes",
                "description": "The newest warplanes test contract"
            }
        },
        "sellerId": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
        "sellerAddress": "0x5F81D2867996baFee01e109fBcC8e3AD2Edf044E",
        "startDate": "2020-10-26T13:33:15.908141Z",
        "endDate": "2020-11-05T13:33:15.908158Z",
        "type": "SALE",
        "status": "FINALIZING_OFFER",
        "dataToSign": "18ec506b-1d11-4f94-95f4-e19d89f93da1_0x5F81D2867996baFee01e109fBcC8e3AD2Edf044E_0xe885A1cD1b67bDC352A113AB2e6A5Fc6C924F888_57896044618658097711785492504343953927655839433583097410118915826251869454343",
        "txInCustody": "0x4f7fd89195bcd4f84b35c873cbf5a013df948fa1fd71f89d9d0f3c9f1d500c20",
        "txOutOfCustody": "0x2e6b7e9923fb9348ef6ce55f472668c71b193b46468e79879639230483d525af",
        "createdOn": "2020-10-26T13:33:15.943301Z",
        "createdBy": "250f3885-d69d-4ef3-9eae-aebbb10f5b3e",
        "price": 200,
        "buyerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "buyerWalletAddress": "0x8D6331D6C5ba3306961F0b4Ea13ff13aa43560b9",
        "externalBuyerId": "yourUserIdentifier",
        "soldOn": "2020-11-05T09:28:48.569562Z"
    }
}
```
