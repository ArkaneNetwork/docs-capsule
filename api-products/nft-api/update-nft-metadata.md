---
description: Endpoint that allows you to update the metadata of a NFT template (Token type)
---

# Update NFT metadata

Note this endpoint allows you to update the metadata, some attributes are defined on the NFT contract and therefore not updatable.

{% hint style="warning" %}
Here is a list of the attributes that **can not be updated**:

* fungible
* burnable
* maxSupply
{% endhint %}

## Endpoint: PUT

```javascript
https://api-business.arkane.network/api/apps/{{application_id}}/contracts/{{contract_id}}/token-types/{{tokenTypeId}}/metadata
```

## Body

```javascript
{
  "name" : "Chuck (Updated)",
  "description" : "Chuck is a Male Tall Chicken (Updated)",
  "image": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
  "backgroundColor" : "#021200",
  "externalUrl" : "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
  "animationUrls" : [
      {"type": "video", "value" : "https://img.arkane.network/marketing/SpaceChickens/space_chickens_trailer.mp4"}
  ],
    "attributes" : [
      {"type": "property", "name" : "Talent", "value": "Leadership"},
      {"type": "property", "name" : "Allergic", "value": "Monstonuts"},
      {"type": "property", "name" : "Hobby", "value": "Scouts"},
      {"type": "stat", "name" : "Cool", "value": "9", "maxValue": "10"},
      {"type": "stat", "name" : "Daring", "value": "8", "maxValue": "10"},
      {"type": "stat", "name" : "Noise", "value": "8", "maxValue": "10"},
      {"type": "stat", "name" : "Age", "value": "3"}
  ]
}
```

## Returns

```javascript
{
    "name": "Chuck (Updated)",
    "description": "Chuck is a Male Tall Chicken (Updated)",
    "image": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
    "imagePreview": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
    "imageThumbnail": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
    "backgroundColor": "#021200",
    "background_color": "#021200",
    "animationUrl": "https://img.arkane.network/marketing/SpaceChickens/space_chickens_trailer.mp4",
    "animation_url": "https://img.arkane.network/marketing/SpaceChickens/space_chickens_trailer.mp4",
    "externalUrl": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
    "external_url": "https://previews.123rf.com/images/bankrx/bankrx1810/bankrx181000576/110633429-grunge-green-updated-word-with-star-icon-round-rubber-seal-stamp-on-white-background.jpg",
    "animationUrls": [
        {
            "type": "video",
            "value": "https://img.arkane.network/marketing/SpaceChickens/space_chickens_trailer.mp4"
        }
    ],
    "maxSupply": 25,
    "attributes": [
        {
            "type": "property",
            "name": "Talent",
            "value": "Leadership",
            "traitType": "Talent",
            "trait_type": "Talent"
        },
        {
            "type": "property",
            "name": "Allergic",
            "value": "Monstonuts",
            "traitType": "Allergic",
            "trait_type": "Allergic"
        },
        {
            "type": "property",
            "name": "Hobby",
            "value": "Scouts",
            "traitType": "Hobby",
            "trait_type": "Hobby"
        },
        {
            "type": "stat",
            "name": "Cool",
            "value": "9",
            "maxValue": "10",
            "displayType": "number",
            "display_type": "number",
            "traitType": "Cool",
            "trait_type": "Cool"
        },
        {
            "type": "stat",
            "name": "Daring",
            "value": "8",
            "maxValue": "10",
            "displayType": "number",
            "display_type": "number",
            "traitType": "Daring",
            "trait_type": "Daring"
        },
        {
            "type": "stat",
            "name": "Noise",
            "value": "8",
            "maxValue": "10",
            "displayType": "number",
            "display_type": "number",
            "traitType": "Noise",
            "trait_type": "Noise"
        },
        {
            "type": "stat",
            "name": "Age",
            "value": "3",
            "displayType": "number",
            "display_type": "number",
            "traitType": "Age",
            "trait_type": "Age"
        }
    ],
    "contract": {
        "address": "0x7940e73832403de364568ce406bd4792097b6594",
        "name": "Space Chickens",
        "symbol": "SPACECHICKS",
        "image": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "image_url": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
        "externalLink": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "external_link": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "external_url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "media": [
            {
                "type": "unknown",
                "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
            }
        ],
        "type": "ERC_1155"
    },
    "asset_contract": {
        "address": "0x7940e73832403de364568ce406bd4792097b6594",
        "name": "Space Chickens",
        "symbol": "SPACECHICKS",
        "image": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "imageUrl": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "image_url": "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
        "description": "Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
        "externalLink": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "external_link": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "external_url": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
        "media": [
            {
                "type": "unknown",
                "value": "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"
            }
        ],
        "type": "ERC_1155"
    },
    "fungible": true
}
```

## Advanced

{% hint style="info" %}
For more information on configuration options in the NFT template, such as **adding media**, defining a **max supply**, and **much more** please read [NFT Configuration](../../advanced/nft-metadata/).
{% endhint %}
