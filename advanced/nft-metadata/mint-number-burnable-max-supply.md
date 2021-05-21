---
description: Unique mint number
---

# Mint number

## Mint number

When creating the NFT template you can add advanced parameters to the JSON configuration, such as defining if each NFT created from the template will have a unique mint number. Starting with 1 for the first mint and increased by +1 for each following NFT that is minted from that template. This generates truly unique NFTs as each version of your template has a unique number. Think about a Legendary sword [🗡️](https://emojipedia.org/dagger/)in your favorite game, only 5 exist and each Sword is unique. This is what we call a Non-fungible NFT. 

{% hint style="info" %}
Please note that the mint number is stored on the contract, therefore on-chain, it can not be altered.
{% endhint %}

On the other spectrum, we have what we call a Fungible NFT, to explain the difference we go back to your favorite game, but instead of a legendary sword, we are minting 100.000 fish 🐟NFTs. Used to heal your character. In the scenario, each fish is the same like each Bitcoin or Dollar is the same. In this case, we speak about Fungible NFT. 

Depending on which type of NFT you can add the boolean field `fungible` to your NFT template configuration. It is optional and default it is set to `false`. Setting it to true will allow you to create Fungible NFTs.

{% hint style="info" %}
Please note when creating a Fungible NFT template you are required to use the [Mint Fungible NFT ](../../api-products/nft-api/mint-fungible-nft.md)endpoint.
{% endhint %}

## Data Structure

### Signature

```java
"fungible" : boolean

```

### Example

```java
{
  "name" : "Chuck Darling",
  "description" : "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
  "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
  "fungible" : true,
  "maxSupply" : "25",
  "externalUrl" : "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
  "animationUrls" : [
       {"type": "video", "value" : "http://img.arkane.network/chuck_trailer.mp4"},
       {"type": "audio", "value" : "http://img.arkane.network/chuck_soundtrack.mp3"}
  ],
  "attributes" : [
      {"type": "property", "name" : "Talent", "value": "Leadership"},
      {"type": "property", "name" : "Allergic", "value": "Monstonuts"},
      {"type": "property", "name" : "Hobby", "value": "Scouts"},
      {"type": "stat", "name" : "Cool", "value": "9", "maxValue": "10"},
      {"type": "stat", "name" : "Daring", "value": "8", "maxValue": "10"},
      {"type": "stat", "name" : "Noise", "value": "8", "maxValue": "10"},
      {"type": "stat", "name" : "Age", "value": "3"},
      {"type": "boost", "name" : "Crafting", "value": "+5"},
      {"type": "boost", "name" : "Leadership", "value": "+10"}
  ]
}
```

