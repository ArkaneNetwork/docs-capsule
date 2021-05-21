---
description: Metadata on the level of the NFT contract
---

# Collection Info

Collection info is metadata about the collection, the brand, the company to which the NFT belongs. Unlike all other metadata, the collection info is not stored in the metadata of the NFT, but rather in the metadata of the NFT contract. It allows us to add information such as the name and description of a collection as well as certain forms of media such as a logo and a banner, social channels, even a YouTube video.

![Information about the contract of a certain NFT](../../.gitbook/assets/image%20%288%29.png)

## Data Structure

### Signature

```java
{
	"name": string, // Name of the collection
	"description": string, // Description of the collection
	"chain" : string, // Blockchain that hosts the contract
	"symbol" : string, // Symbol related to the contract
  "image" : string // Logo of the collection,
  "externalUrl": string // CTA link,
  "media" : [
      {"type": "image", "value" : string }, // Will be used as a hero/banner image
      {"type": "youtube", "value" : string }, // Replaces the hero/banner image with an embeded video
      {"type": "instagram", "value" : string }, // Adds Instagram social link
      {"type": "twitter", "value" : string } // Adds Twitter social link
    ],
}

```

### Example

```java
{
	"name": "Space Chickens",
	"description":"Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
	"chain" : "MATIC",
	"symbol" : "SPACECHICKS",
  "image" : "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
  "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
  "media" : [
      {"type": "image", "value" : "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"},
      {"type": "youtube", "value" : "https://www.youtube.com/embed/1dFgZwpeokk"},
      {"type": "instagram", "value" : "https://www.instagram.com/spacechickes"},
      {"type": "twitter", "value" : "https://twitter.com/spacechickes"}
    ],
}
```

![](../../.gitbook/assets/image%20%2813%29.png)

### Properties

The properties section is mostly used to display text-based attributes such as the type or category of an item, a team, certain year, rarity, ...

![](../../.gitbook/assets/image%20%2817%29.png)

```java
"attributes" : [
      {"type": "property", "name" : "Talent", "value": "Leadership"},
      {"type": "property", "name" : "Allergic", "value": "Monstonuts"},
      {"type": "property", "name" : "Hobby", "value": "Scouts"}
  ]
```

### Stats

The stats section is used to display certain stats and metrics, such as the level of a certain item, the amount of defense, power, or top speed a certain item possesses.

When a stat also has a max value defined it will be visualized as a progress bar, otherwise, it will be shown as a card.

![](../../.gitbook/assets/image%20%2816%29.png)

```java
"attributes" : [
      {"type": "stat", "name" : "Age", "value": "3"},
      {"type": "stat", "name" : "Cool", "value": "9", "maxValue":"10"},
      {"type": "stat", "name" : "Daring", "value": "8", "maxValue":"10"},
      {"type": "stat", "name" : "Noise", "value": "8", "maxValue":"10"}
  ]
```

### Boosts

Boosts is a category to display gains that are achieved by possessing or using a certain item. It usually is accompanied by a positive or negative identifier. Examples of a boost are the increase or decrease of speed, armor but equally, it can be a reduction of certain fees or an increase in chance.

![](../../.gitbook/assets/image%20%2814%29.png)

```java
"attributes" : [
      {"type": "boost", "name" : "Crafting", "value": "+5"},
      {"type": "boost", "name" : "Leadership", "value": "+10"}
  ]
```

## Data Structure

### Signature

```java
"attributes": [
    {
      "type": "property",
      "name": string, 
      "value": string
    }, 
    {
      "type": "stat",
      "name": string, 
      "value": string,
      "maxValue": string
    }, 
    {
      "type": "stat",
      "name": string, 
      "value": string,
    },
    {
      "type": "boost",
      "name": string, 
      "value": string
    }
]

```

### Example

```java
"attributes": [
    {
      "type": "property",
      "name": "Type", 
      "value": "Hero"
    }, 
    {
      "type": "property",
      "name": "Team", 
      "value": "Avengers"
    },
    {
      "type": "stat",
      "name": "Level", 
      "value": "7"
    }, 
    {
      "type": "stat",
      "name": "Strength", 
      "value": "88",
      "maxValue": "93"
    }, 
    {
      "type": "stat",
      "name": "Speed", 
      "value": "74",
      "maxValue": "100"
    },
    {
      "type": "boost",
      "name": "Defence", 
      "value": "+5"
    }, 
    {
      "type": "boost",
      "name": "Rage", 
      "value": "-5"
    }
]
```

### Compatibility

In order to be compatible with the NFT standards on the market, in terms of attributes, our system takes the above JSON structure and transforms it into a JSON that is compatible with the following attribute standards:

* [ERC721](https://eips.ethereum.org/EIPS/eip-721)
* [ERC115](https://eips.ethereum.org/EIPS/eip-1155)
* [OpenSea's metadata standard](https://docs.opensea.io/docs/metadata-standards)

This results in an easy-to-use property structure, which provides consistency and compatibility with any NFT service on the market, such as wallets, marketplaces,... 

