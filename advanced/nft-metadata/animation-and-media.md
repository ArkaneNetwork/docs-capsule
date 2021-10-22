---
description: Adding Video and Audio to the mix
---

# Animation & Media

NFT can be enriched by adding video or audio content. This allows NFT services to take advantage of this enriched media content, and for the creator it allows them to share more information about the content and value of the NFT.

![Example of an NFT that is enriched with an audio file](<../../.gitbook/assets/image (16).png>)

## animationUrls

Audio and video can be added to an NFT by configuring the `animationUrls[]` attribute. The attribute is a key/value array where the key defines the type of media that is added. The value is the location where the media can be found. The following keys are currently supported:

* image&#x20;
* audio
* video&#x20;

Based on the key, the following media format are supported by Arkane.

* **image**:** **gif / png / jpg / jpeg / bmp / webp / svg
* **audio**: mp3 / wav / oga
* **video**: mp4 / webm / m4v / ogv / ogm / ogg

Since the `animationUrls[]` is an array it is possible to add more than one piece of media to an NFT.&#x20;

```java
"animationUrls" : [
       {"type": "video", "value" : "http://img.arkane.network/chuck_trailer.mp4"},
       {"type": "audio", "value" : "http://img.arkane.network/chuck_soundtrack.mp3"}
  ]
```

![Example of an NFT that is enriched with a video file](<../../.gitbook/assets/image (17).png>)

## Data Structure

### Signature

```java
"animationUrls" : [
      {
       "type": "image", 
       "value" : string
      },
      {
       "type": "video", 
       "value" : string
      },
      {
       "type": "audio", 
       "value" : string
      }
  ],

```

### Example

```java
"animationUrls" : [
      {
       "type": "image", 
       "value" : "https//img.arkane.network/nft.jpg"
      },
      {
       "type": "video", 
       "value" : "https//video.arkane.network/nft.mp4"
      },
      {
       "type": "audio", 
       "value" : "https//audio.arkane.network/nft.mp3"
      }
  ],
```

### Compatibility

In order to be compatible with the NFT standards on the market, in terms of animation, our system takes the above JSON structure and transforms it into a JSON that is compatible with the following animation standards:

* [ERC721](https://eips.ethereum.org/EIPS/eip-721)
* [ERC115](https://eips.ethereum.org/EIPS/eip-1155)
* [OpenSea's metadata standard](https://docs.opensea.io/docs/metadata-standards)

This results in an easy-to-use property structure, which provides consistency and compatibility with any NFT service on the market, such as wallets, marketplaces,...&#x20;

{% hint style="info" %}
Please note that most NFT service can only handle one animationUrl, therefore it is recommended to put the most important media as the first element in the `animationUrls` array.
{% endhint %}
