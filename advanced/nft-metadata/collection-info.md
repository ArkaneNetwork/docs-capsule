---
description: Metadata on the level of the NFT contract
---

# Collection Info

Collection info is metadata about the collection, the brand, the company to which the NFT belongs. Unlike all other metadata, the collection info is not stored in the metadata of the NFT, but rather in the metadata of the NFT contract. It allows us to add information such as the name and description of a collection as well as certain forms of media such as a logo and a banner, social channels, even a YouTube video.

![Information about the contract of a certain NFT](<../../.gitbook/assets/image (20).png>)

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
