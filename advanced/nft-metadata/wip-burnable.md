---
description: Allow an NFT to get burned 🔥
---

# Burnable

## Burnable

When creating the NFT template you can add advanced parameters to the JSON configuration, such as defining if an NFT can be burned. Burning an NFT effectively destroys the token and removes it entirely from the blockchain. When you burn an NFT, the transaction is irreversible.

You can define if NFTs from a certain NFT template can be burned by adding the optional field `burnable` to your  NFT template configuration. Default it is set to false.

{% hint style="info" %}
Please note that `burnable` is configured, stored, and track on-chain, meaning once set it can not be altered.
{% endhint %}

## Data Structure

### Signature

```java
"burnable": boolean
```

### Example

```java
{
  "name" : "Chuck Darling",
  "description" : "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
  "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
  "maxSupply" : "25",
  "burnable": true,
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
