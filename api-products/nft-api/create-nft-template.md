---
description: >-
  This endpoint allows you to create an NFT template which you can you to mint
  NFTs from. A more technical representation of the template is token type.
---

# Create NFT template

## Endpoint: POST

```javascript
https://api-business.arkane.network/api/apps/{{application_id}}/contracts/{{contract_id}}/token-types
```

## Body

```javascript
{
  "name" : "Chuck The Rooster",
  "description" : "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
  "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
  "externalUrl" : "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
  "fungible": false,
  "attributes" : [
      {"type": "property", "name" : "Talent", "value": "Leadership"},
      {"type": "property", "name" : "Allergic", "value": "Monstonuts"},
      {"type": "property", "name" : "Hobby", "value": "Scouts"}
  ]
}
```

## Returns

```javascript
{
    "id": 1,
    "confirmed": false,
    "name": "Chuck The Rooster",
    "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
    "fungible": false,
    "burnable": false,
    "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
    "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "imageThumbnail": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "imagePreview": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "currentSupply": 0,
    "animationUrls": [],
    "attributes": [
        {
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
        }
    ],
    "transactionHash": "0x36582ee04ef2b4570f381b59971deb2d2e698fb77724deb193333223119403c4"
```

## Advanced

{% hint style="info" %}
For more information on configuration options in the NFT template, such as **adding media**, defining a **max supply**, and **much more** please read [NFT Configuration](../../advanced/nft-metadata/).
{% endhint %}

