---
description: Endpoint that allows you to read contract functions
---

# Read contract

{% swagger baseUrl="https://api.arkane.network" path="/api/contracts/read" method="post" summary="Read a contract " %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="inputs.type" type="string" %}
Type of the input parameter (ex. uint256)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="inputs.value" type="string" %}
Value of the input parameter. This needs to be passed as a string value
{% endswagger-parameter %}

{% swagger-parameter in="body" name="inputs" type="array" %}
Array of inputs needed to call the function
{% endswagger-parameter %}

{% swagger-parameter in="body" name="functionName" type="string" %}
Contract function to call
{% endswagger-parameter %}

{% swagger-parameter in="body" name="secretType" type="string" required="true" %}
On which blockchain the tx will be executed
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletAddress" type="string" %}
Wallet address, available if required
{% endswagger-parameter %}

{% swagger-parameter in="body" name="outputs" required="true" %}
Array of expected outputs
{% endswagger-parameter %}

{% swagger-parameter in="body" name="outputs.type" required="true" %}
Type of output 
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```java
{
    "success": true,
    "result": [
        {
            "type": "uint256",
            "value": 1
        }
    ]
}
```
{% endswagger-response %}
{% endswagger %}

## Examples&#x20;

### Get Balance of

This example will get the balance of a certain NFT for a specific wallet

```javascript
POST: https://api.arkane.network/api/contracts/read
```

#### Request Body

```java
{
    "secretType": "MATIC",
    "walletAddress": "0x0000000000000000000000000000000000000000",
    "contractAddress": "0xE80F3baA739c18fd4eBf97716529a4b85BE464Dd",
    "functionName": "balanceOf",
    "inputs": [
        {
            "type": "address",
            "value": "0x427d0addaa77d8bb871dbea3458dea4b5198730c"
        },
        {
            "type": "uint256",
            "value": "202"
        }
    ],
    "outputs": [
        {
            "type": "uint256"
        }
    ]
}
```

#### Response

```java
{
    "success": true,
    "result": [
        {
            "type": "uint256",
            "value": 1
        }
    ]
}
```



### Get Mint  Number&#x20;

This example will get the mint number for a specific NFT.

```javascript
POST : https://api.arkane.network/api/contracts/read
```

#### Request Body

```java
{
    "secretType": "MATIC",
    "walletAddress": "0x0000000000000000000000000000000000000000",
    "contractAddress": "0xf86013ac3a23d26efb3337b4d63de6e6ec2a9861",
    "functionName": "mintNumber",
    "inputs": [
        {
            "type": "uint256",
            "value": "51"
        }
    ],
    "outputs": [
        {
            "type": "uint256"
        }
    ]
}
```

#### Response

```java
{
    "success": true,
    "result": [
        {
            "type": "uint256",
            "value": 2
        }
    ]
}
```



### Get Contract URI

This example will fetch the contract URI, which contains the metadata, for a specific contract.

```javascript
POST : https://api.arkane.network/api/contracts/read
```

#### Request Body

```java
{
    "secretType": "MATIC",
    "walletAddress": "0x0000000000000000000000000000000000000000",
    "contractAddress": "0x8c53de6a889cf0a3151168c3e84263c982d09a2f",
    "functionName": "contractURI",
    "outputs": [
        {
            "type": "string"
        }
    ]
}
```

#### Response

```java
{
    "success": true,
    "result": [
        {
            "type": "string",
            "value": "https://metadata.arkane.network/api/apps/0ed3a778-4f11-4cdf-b3cc-45f3225a9065/contracts/76/metadata"
        }
    ]
}
```
