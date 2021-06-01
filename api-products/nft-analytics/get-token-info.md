---
description: >-
  Retrieve the NFT token information based on the NFT contract address and the
  token id.
---

# Get token info

{% api-method method="get" host="https://<chain>-azrael.arkane.network" path="/contracts/:tokenContract/tokens/:tokenId" %}
{% api-method-summary %}
Get token info
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="tokenId" type="string" required=true %}
Id of the token
{% endapi-method-parameter %}

{% api-method-parameter name="tokenContract" type="string" required=true %}
Address of the token contract
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "contract": {
        "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
        "contractType": "ERC_721",
        "name": "Neon District Season One Item",
        "symbol": "NDITEM1"
    },
    "uri": "https://portal.neondistrict.io/api/getNft/158456328127582242520246418699",
    "metadata": "{\"external_url\":\"https://portal.neondistrict.io/asset/158456328127582242520246418699\",\"name\":\"Ruiner\",\"image\":\"https://neon-district-season-one.s3.amazonaws.com/images/blkoriginruiner-common-thrusting-sml-thumb.png\",\"description\":\"A weapon found within Neon District.\\n\\nA Neon District: Season One game item, playable on https://portal.neondistrict.io.\\n\\nNeon District is a free-to-play cyberpunk role-playing game. Collect characters and gear, craft and level up teams, and battle against other players through competitive multiplayer and in turn-based combat.\",\"attributes\":[{\"trait_type\":\"type\",\"value\":\"Weapon\"},{\"trait_type\":\"rarity\",\"value\":\"Common\"},{\"trait_type\":\"level\",\"value\":5},{\"display_type\":\"number\",\"trait_type\":\"Season\",\"value\":1},{\"display_type\":\"boost_number\",\"trait_type\":\"Mech\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Nano\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Attack\",\"value\":21},{\"display_type\":\"boost_number\",\"trait_type\":\"Health\",\"value\":435},{\"display_type\":\"boost_number\",\"trait_type\":\"Defense\",\"value\":54},{\"display_type\":\"boost_number\",\"trait_type\":\"Hacking\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Stealth\",\"value\":22},{\"display_type\":\"boost_number\",\"trait_type\":\"Tactics\",\"value\":22},{\"trait_type\":\"Card\",\"value\":\"Thread the Needle\"},{\"trait_type\":\"Card\",\"value\":\"Fleche Eater\"},{\"trait_type\":\"Card\",\"value\":\"Undermine\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Penetrate\"},{\"trait_type\":\"Card\",\"value\":\"Penetrate\"},{\"trait_type\":\"Card\",\"value\":\"Double Tap\"},{\"trait_type\":\"Card\",\"value\":\"Double Tap\"}]}"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

```javascript
https://matic-azrael.arkane.network/contracts/0x7227e371540cf7b8e512544ba6871472031f3335/tokens/158456328127582242520246418699
```

#### Response

```javascript
{
    "contract": {
        "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
        "contractType": "ERC_721",
        "name": "Neon District Season One Item",
        "symbol": "NDITEM1"
    },
    "uri": "https://portal.neondistrict.io/api/getNft/158456328127582242520246418699",
    "metadata": "{\"external_url\":\"https://portal.neondistrict.io/asset/158456328127582242520246418699\",\"name\":\"Ruiner\",\"image\":\"https://neon-district-season-one.s3.amazonaws.com/images/blkoriginruiner-common-thrusting-sml-thumb.png\",\"description\":\"A weapon found within Neon District.\\n\\nA Neon District: Season One game item, playable on https://portal.neondistrict.io.\\n\\nNeon District is a free-to-play cyberpunk role-playing game. Collect characters and gear, craft and level up teams, and battle against other players through competitive multiplayer and in turn-based combat.\",\"attributes\":[{\"trait_type\":\"type\",\"value\":\"Weapon\"},{\"trait_type\":\"rarity\",\"value\":\"Common\"},{\"trait_type\":\"level\",\"value\":5},{\"display_type\":\"number\",\"trait_type\":\"Season\",\"value\":1},{\"display_type\":\"boost_number\",\"trait_type\":\"Mech\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Nano\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Attack\",\"value\":21},{\"display_type\":\"boost_number\",\"trait_type\":\"Health\",\"value\":435},{\"display_type\":\"boost_number\",\"trait_type\":\"Defense\",\"value\":54},{\"display_type\":\"boost_number\",\"trait_type\":\"Hacking\",\"value\":12},{\"display_type\":\"boost_number\",\"trait_type\":\"Stealth\",\"value\":22},{\"display_type\":\"boost_number\",\"trait_type\":\"Tactics\",\"value\":22},{\"trait_type\":\"Card\",\"value\":\"Thread the Needle\"},{\"trait_type\":\"Card\",\"value\":\"Fleche Eater\"},{\"trait_type\":\"Card\",\"value\":\"Undermine\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Buckler Up\"},{\"trait_type\":\"Card\",\"value\":\"Penetrate\"},{\"trait_type\":\"Card\",\"value\":\"Penetrate\"},{\"trait_type\":\"Card\",\"value\":\"Double Tap\"},{\"trait_type\":\"Card\",\"value\":\"Double Tap\"}]}"
}
```

