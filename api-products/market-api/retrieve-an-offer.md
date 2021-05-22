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

