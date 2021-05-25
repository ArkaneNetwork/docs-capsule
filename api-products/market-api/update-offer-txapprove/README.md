---
description: Endpoint to pass the transaction hash of the Approve transaction
---

# Update offer: TxApprove

In order for the market to take an NFT into custody, the market requires the end user to execute a contract call, allowing the market to move the NFT. Since the market doesn't know the end-users of the client, it is up to the client to ask the user to perform the Approve transaction. Once the user has launched the Approve transaction the client sends the transaction hash of that transaction back to the market for validation.

Since there are multiple variants and standards of NFT contracts it can be difficult for a client to know for each NFT contract which function to call and which input parameter each function might need. To overcome that specific pain the market also provides an endpoint that returns that required information, allowing the client to easily query what they need to forward to their end-users. 

{% page-ref page="get-prepared-transaction.md" %}

{% api-method method="patch" host="https://api.arkane.market" path="/offers/:offerId/txapprove" %}
{% api-method-summary %}
Update offer: TxApprove
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="offerId" type="string" required=true %}
ID of the offer that needs the update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="txApprove" type="string" required=true %}
Transaction hash of the Approve transaction executed by the end-user.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the result of the call and the wallet 
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "id": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5",
        "nft": {
            "tokenId": "2",
            "address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
            "chain": "ETHEREUM",
            "name": "Cauliflower Pizza",
            "description": "Awesome cauliflower crust pizza with cured pepperoni. Found on a BBS in the early 80s.",
            "imageUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A",
            "url": "",
            "imagePreviewUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s250",
            "imageThumbnailUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s128",
            "attributes": [
                {
                    "traitType": "topping",
                    "value": "cheese",
                    "traitCount": 4
                },
                {
                    "traitType": "crust",
                    "value": "cauliflower",
                    "traitCount": 2
                },
                {
                    "traitType": "topping",
                    "value": "pepperoni",
                    "traitCount": 2
                },
                {
                    "traitType": "level",
                    "value": "7",
                    "traitCount": 1
                },
                {
                    "traitType": "fuel",
                    "value": "3.4",
                    "traitCount": 1
                },
                {
                    "traitType": "cauliflower_power",
                    "value": "80",
                    "displayType": "boost_number",
                    "traitCount": 1
                },
                {
                    "traitType": "bellyfat_increase",
                    "value": "3",
                    "displayType": "boost_percentage",
                    "traitCount": 1
                }
            ],
            "contract": {
                "chain": "ETHEREUM",
                "address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
                "count": 0,
                "name": "CryptoPizza Shop",
                "description": "In honor of the dude who paid 10k BTC for two large pizzas in 2010, I'm proud to announce the first ever CryptoPizza Shop! Collect these slices - more to be added soon, but these OG CryptoPizza Slices will go down in history!",
                "symbol": "OSC",
                "imageUrl": "https://rinkeby-storage.opensea.io/0x492aef91afb79efaa508debbed7b3e21069d13e3-1561429292.png"
            }
        },
        "sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "sellerAddress": "0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690",
        "startDate": "2020-10-21T14:46:09.252659Z",
        "endDate": "2020-10-31T14:46:09.252674Z",
        "type": "SALE",
        "status": "NEW",
        "dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
        "txApprove": "0xd5234cc910c382a4807d94b5af3be68f62ecac867bef9a61e984dfad08257a44",
        "createdOn": "2020-10-21T14:46:09.305261Z",
        "createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "price": 25
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Note that in order to move an offer from state **NEW** to state **READY**, the offer will need a 2nd update, which is [Update offer: Signature](../update-offer-signature.md).
{% endhint %}

{% hint style="warning" %}
**Note:** The order is important. First the TxApprove, then the Signature. 
{% endhint %}

## TxApprove not always required

The Approve transaction is not always required, when a wallet has approved the market for a specific NFT contract in the past the wallet will not be required to approve the market a second time. More concrete if a user has approved the market to take an NFT of a certain NFT contract into custody he will not have to approve the market next time he wants to sell a different NFT of the same NFT contract.

{% hint style="info" %}
In this case the [Update offer: TxApprove](./) step can be skipped and moved directly to [Update offer: Signature](../update-offer-signature.md).
{% endhint %}

### How can you know if the Approve is required?

An easy way is to call the [Get prepared Approve tx](get-prepared-transaction.md) endpoint. When the result set is empty it means the Approve step can be skipped. If the result set contains data, then the Approve still needs to happen.

{% page-ref page="get-prepared-transaction.md" %}

## Example

#### Request

```javascript
https://api.arkane.market/offers/b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5/txapprove
```

#### Request Body

```javascript
{
    "txApprove": "0x7c7fe6ffa8100851e00676ebfea524dc6c666e017da67f07ac4f93e48d1329af"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "id": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5",
        "nft": {
            "tokenId": "2",
            "address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
            "chain": "ETHEREUM",
            "name": "Cauliflower Pizza",
            "description": "Awesome cauliflower crust pizza with cured pepperoni. Found on a BBS in the early 80s.",
            "imageUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A",
            "url": "",
            "imagePreviewUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s250",
            "imageThumbnailUrl": "https://lh3.googleusercontent.com/0Dw7pMcyX_m7T_6q3zzrvjmYMg-Matgg8c42DTGvviRDI8M7fa3Ot9siVfhzE0gqolLshVp2O6T3QdccmVblMurg7A=s128",
            "attributes": [
                {
                    "traitType": "topping",
                    "value": "cheese",
                    "traitCount": 4
                },
                {
                    "traitType": "crust",
                    "value": "cauliflower",
                    "traitCount": 2
                },
                {
                    "traitType": "topping",
                    "value": "pepperoni",
                    "traitCount": 2
                },
                {
                    "traitType": "level",
                    "value": "7",
                    "traitCount": 1
                },
                {
                    "traitType": "fuel",
                    "value": "3.4",
                    "traitCount": 1
                },
                {
                    "traitType": "cauliflower_power",
                    "value": "80",
                    "displayType": "boost_number",
                    "traitCount": 1
                },
                {
                    "traitType": "bellyfat_increase",
                    "value": "3",
                    "displayType": "boost_percentage",
                    "traitCount": 1
                }
            ],
            "contract": {
                "chain": "ETHEREUM",
                "address": "0x492aef91afb79efaa508debbed7b3e21069d13e3",
                "count": 0,
                "name": "CryptoPizza Shop",
                "description": "In honor of the dude who paid 10k BTC for two large pizzas in 2010, I'm proud to announce the first ever CryptoPizza Shop! Collect these slices - more to be added soon, but these OG CryptoPizza Slices will go down in history!",
                "symbol": "OSC",
                "imageUrl": "https://rinkeby-storage.opensea.io/0x492aef91afb79efaa508debbed7b3e21069d13e3-1561429292.png"
            }
        },
        "sellerId": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "sellerAddress": "0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690",
        "startDate": "2020-10-21T14:46:09.252659Z",
        "endDate": "2020-10-31T14:46:09.252674Z",
        "type": "SALE",
        "status": "NEW",
        "dataToSign": "b91c6f5f-5ebd-4941-99c1-94e9d1cbd9d5_0xdb7c22EA49EF93F753F2ed4c9E1A2589aC6E7690_0xb06b3f1e824BD7eFC0BCe584cF6B772dC0Ff7C75_2",
        "txApprove": "0xd5234cc910c382a4807d94b5af3be68f62ecac867bef9a61e984dfad08257a44",
        "createdOn": "2020-10-21T14:46:09.305261Z",
        "createdBy": "7cbc2bd3-b3d7-4d8e-bda8-173e56189f75",
        "price": 25
    }
}
```

