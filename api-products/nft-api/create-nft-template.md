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
    "name": "Chuck The Rooster",
    "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
    "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
    "backgroundColor": "#FFFFFF",
    "attributes": [
        {
            "type": "property",
            "name": "Talent",
            "value": "Leadership"
        }
    ]
}
```

{% hint style="info" %}
Venly offers more complex NFT configurations, such as setting a **max supply**, adding **mint numbers**, and **IPFS** storage.&#x20;

For a full overview please check out [NFT Configuration](../../advanced/nft-metadata/).
{% endhint %}

## Returns

```javascript
{
    "id": 51,
    "confirmed": false,
    "name": "Chuck The Rooster",
    "description": "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
    "fungible": false,
    "burnable": false,
    "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
    "backgroundColor": "#FFFFFF",
    "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "imageThumbnail": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "imagePreview": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
    "maxSupply": 25,
    "currentSupply": 0,
    "animationUrls": [
        {
            "type": "video",
            "value": "http://img.arkane.network/chuck_trailer.mp4"
        },
        {
            "type": "audio",
            "value": "http://img.arkane.network/chuck_soundtrack.mp3"
        }
    ],
    "attributes": [
        {
            "type": "property",
            "name": "Talent",
            "value": "Leadership"
        }
    ],
    "transactionHash": "0xec345e382121ff5372351257f1a48a0f550064f974bff01cf7557eb55700a79e"
}
```

