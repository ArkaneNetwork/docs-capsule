---
description: Retrieve the NFT contract information based on the contract address
---

# Get NFT contract

{% swagger baseUrl="https://api.arkane.network" path="/api/nonfungibles/:secretType/:tokenContract" method="get" summary="Get token contract" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="tokenContract" type="string" required="true" %}
Address of the token contract
{% endswagger-parameter %}

{% swagger-parameter in="path" name="secretType" type="SecretType" required="true" %}
The secret type (ex HEDERA)
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns the result of the call and the wallet " %}
```javascript
{
    "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
    "contractType": "ERC_721",
    "name": "Neon District Season One Item",
    "symbol": "NDITEM1"
}
```
{% endswagger-response %}
{% endswagger %}

### Example

#### Request

```javascript
https://api.arkane.network/api/nonfungibles/HEDERA/0.0.2850147/25
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "name": "Digimon",
        "description": null,
        "address": "0.0.2850147",
        "symbol": "DGM",
        "media": null,
        "type": "NON_FUNGIBLE_UNIQUE",
        "verified": false,
        "premium": false,
        "categories": [],
        "url": null,
        "imageUrl": null
    }
}
```

{% hint style="info" %}
This API also supports NFT contracts that host their metadata on **IPFS** or store it as a **base64** string in the contract itself.&#x20;
{% endhint %}

{% content-ref url="../../deep-dive-1/object-reference/secrettype.md" %}
[secrettype.md](../../deep-dive-1/object-reference/secrettype.md)
{% endcontent-ref %}

{% content-ref url="../../deep-dive-1/object-reference/nftcontract.md" %}
[nftcontract.md](../../deep-dive-1/object-reference/nftcontract.md)
{% endcontent-ref %}
