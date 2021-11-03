---
description: Available options for storing NFT metadata 💾
---

# Metadata Storage

## Storage

When creating the NFT template you can add advanced parameters to the JSON configuration, such as defining where the metadata of the NFT should be hosted. This can be done by defining the `storage` attribute.

The storage attribute has 3 possible configurations.

**Cloud (default)**

The default option, Venly will generate the metadata file and store it safely in the cloud. This option allows metadata of NFTs to be updated.

**IPFS**

Also with this option, Venly will generate the metadata file, but now it will store the file on IPFS for you. This option will not allow you to update the metadata for that NFT.

**Custom**

The third option is to provide a custom URL. In this option, Venly is not generating, nor taking care of hosting the metadata file for you. You are able to host and construct it any way you like. Note, this option allows you to change your metadata, since you are in control of the hosting, BUT it does not allow you to update the URL towards the metadata. &#x20;

{% hint style="info" %}
Make sure you understand the benefits and limits of each storage option before changing the default behavior.
{% endhint %}

{% hint style="warning" %}
Please note that when using the custom option for storing your metadata, Venly doesn't validate the content of your metadata file and therefore can not guarantee compatibility across the wider blockchain ecosystem.
{% endhint %}

## Data Structure

### Signature

```java
"storage" : 
      {
        "type": string
        "value": string
     }
```

### Example

```json
//The default cloud storage option
"storage" : 
      {
        "type": "cloud"
     }
     
     
//Using IPFS for hosting your metadata
"storage" : 
      {
        "type": "ipfs"
     }


//Provide a custom metadata link
"storage" : 
      {
        "type": "custom"
        "location": "<URL>"
     }
```

### Full example

```java
{
  "name" : "Wed Test - 3 NFT Fungible",
  "description" : "Chuck is a Male Tall Chicken Who is the Leader of The Chicken Siblings. He is Cool, Daring and Wacky. He can be Selfish and Stubborn When it Comes To Challenges, But he is An True Softie when it Comes To His Siblings. In Rebel to the Beak, It revealed that He is Allergic to Monstonuts and In The Good, The Bad and The Clucky, It also Revealed that He Used to Be one Of the Scouts from Slurp,s Little Cowboys Scout Camp along With Finley, Ainta and Hugo. He is the youngest of the three.",
  "image": "https://static.wikia.nocookie.net/parody/images/4/42/74915084_10162764640400387_6139958579186106368_o.jpg",
  "backgroundColor" : "#eeeeee",
  "externalUrl" : "https://en.wikipedia.org/wiki/Space_Chickens_in_Space",
  "animationUrls" : [
      {"type": "video", "value" : "https://img.arkane.network/marketing/SpaceChickens/space_chickens_trailer.mp4"},
      {"type": "audio", "value" : "https://file-examples-com.github.io/uploads/2017/11/file_example_WAV_10MG.wav"}
  ],
  "maxSupply" : "25",
  "fungible" : true,
  "burnable": true,
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
  ],
  "storage" : 
  {
     "type": "ipfs"
  }
}
```
