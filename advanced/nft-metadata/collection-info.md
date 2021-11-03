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
      {"type": "image", "value" : string }, // Will be used as a hero image for your nft
      {"type": "banner", "value" : string }, // Will be used as a banner image for your nft
      {"type": "instagram", "value" : string }, // Adds Instagram social link
      {"type": "twitter", "value" : string } // Adds Twitter social link
   ],
   "owner": Address //Wallet address the will be the owner of the NFT contract
}

```

### Example

```java
{
   "id": 1751, // Reference ID of the contract
   "name": "Space Chickens",
   "description":"Space Chickens in Space is an American-Australian-Mexican-British-Irish animated television series produced by Ánima Estudios in Mexico, Studio Moshi in Australia. A trio of chickens—Chuck, Starley and Finley—are taken from their home and mistakenly enrolled in an elite intergalactic former military academy. It would take all their strength, and teamwork, to survive every escapade they have.",
   "chain" : "MATIC",
   "confirmed": true, // Boolean to indicate if the tx to create the contract has been minted yet.
   "symbol" : "SPACECHICKS",
   "image" : "https://static.wikia.nocookie.net/logopedia/images/a/aa/Space_Chickens_in_Space.jpg",
   "externalUrl": "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
   "media" : [
      {"type": "image", "value" : "https://dg31sz3gwrwan.cloudfront.net/fanart/355763/1357791-0-q80.jpg"},
      {"type": "instagram", "value" : "https://www.instagram.com/spacechickes"},
      {"type": "twitter", "value" : "https://twitter.com/spacechickes"}
    ],
    "owner": "0xF4Cc6E6c585d23585d5F08BDaEE9b85aB658fa95",
    "transactionHash": "0x5b6f718b41b138849f267c9c40b687e28dbe68fc6c50343469e6bd13c578535d" // Transaction that created the contract
}
```

#### **Social links that are supported by the Venly Market**

* Facebook
* Instagram
* Twitter
* Discord
* Twitch
* Medium
* Telegram
* YouTube
