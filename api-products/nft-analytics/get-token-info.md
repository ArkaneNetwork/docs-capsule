---
description: >-
  Retrieve the NFT token information based on the NFT contract address and the
  token id.
---

# Get NFT info

{% swagger baseUrl="https://api.arkane.network" path="/api/nonfungibles/:secretType/:tokenContract/:tokenId" method="get" summary="Get token info" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="tokenId" type="string" required="true" %}
Id of the token
{% endswagger-parameter %}

{% swagger-parameter in="path" name="tokenContract" type="string" required="true" %}
Address of the token contract
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "success": true,
    "result": {
        "id": "25",
        "name": "Agumon",
        "description": "A Reptile Digimon with an appearance resembling a small dinosaur, it has grown and become able to walk on two legs. Its strength is weak as it is still in the process of growing, but it has a fearless and rather ferocious personality. Hard, sharp claws grow from both its hands and feet, and their power is displayed in battle. It also foreshadows an evolution into a great and powerful Digimon. Its Special Move is spitting a fiery breath from its mouth to attack the opponent (Baby Flame).",
        "url": "https://wikimon.net/Agumon",
        "backgroundColor": null,
        "imageUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "imagePreviewUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "imageThumbnailUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "animationUrl": null,
        "animationUrls": [],
        "fungible": false,
        "contract": {
            "name": "Digimon",
            "description": null,
            "address": "0.0.2850147",
            "symbol": "DGM",
            "media": null,
            "type": "NON_FUNGIBLE_UNIQUE",
            "verified": false,
            "premium": false,
            "categories": [],
            "url": null,
            "imageUrl": null
        },
        "attributes": [
            {
                "type": "property",
                "name": "Level",
                "value": "Child",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "property",
                "name": "Type",
                "value": "Reptile",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "property",
                "name": "Attribute",
                "value": "Vaccine",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "stat",
                "name": "Min. weight",
                "value": "15",
                "displayType": "number",
                "traitCount": null,
                "maxValue": 20
            },
            {
                "type": "system",
                "name": "tokenTypeId",
                "value": "1",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            }
        ]
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
https://api.arkane.network/api/nonfungibles/HEDERA/0.0.2850147/25
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "25",
        "name": "Agumon",
        "description": "A Reptile Digimon with an appearance resembling a small dinosaur, it has grown and become able to walk on two legs. Its strength is weak as it is still in the process of growing, but it has a fearless and rather ferocious personality. Hard, sharp claws grow from both its hands and feet, and their power is displayed in battle. It also foreshadows an evolution into a great and powerful Digimon. Its Special Move is spitting a fiery breath from its mouth to attack the opponent (Baby Flame).",
        "url": "https://wikimon.net/Agumon",
        "backgroundColor": null,
        "imageUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "imagePreviewUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "imageThumbnailUrl": "https://wikimon.net/images/6/67/Agumon_cs.jpg",
        "animationUrl": null,
        "animationUrls": [],
        "fungible": false,
        "contract": {
            "name": "Digimon",
            "description": null,
            "address": "0.0.2850147",
            "symbol": "DGM",
            "media": null,
            "type": "NON_FUNGIBLE_UNIQUE",
            "verified": false,
            "premium": false,
            "categories": [],
            "url": null,
            "imageUrl": null
        },
        "attributes": [
            {
                "type": "property",
                "name": "Level",
                "value": "Child",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "property",
                "name": "Type",
                "value": "Reptile",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "property",
                "name": "Attribute",
                "value": "Vaccine",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            },
            {
                "type": "stat",
                "name": "Min. weight",
                "value": "15",
                "displayType": "number",
                "traitCount": null,
                "maxValue": 20
            },
            {
                "type": "system",
                "name": "tokenTypeId",
                "value": "1",
                "displayType": null,
                "traitCount": null,
                "maxValue": null
            }
        ]
    }
}
```
