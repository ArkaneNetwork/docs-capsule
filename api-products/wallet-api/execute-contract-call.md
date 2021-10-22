---
description: >-
  An endpoint to execute a function on a smart contract (write) on any
  (supported) blockchain. As a result, a new transaction will be submitted to
  the network containing the smart contract execution.
---

# Execute contract call

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/execute" method="post" summary="Call a contract" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="chainSpecificFields" type="object" %}
Field that contains chain specific values,  see below.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="inputs.type" type="string" %}
Type of the input parameter (ex. uint256)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="inputs.value" type="string" %}
Value of the input parameter. This needs to be passed as a string value, will be parsed by Arkane
{% endswagger-parameter %}

{% swagger-parameter in="body" name="inputs" type="array" %}
Array of inputs needed to execute the function
{% endswagger-parameter %}

{% swagger-parameter in="body" name="functionName" type="string" %}
Contract function to call
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN related to the wallet ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
CONTRACT_EXECUTION
{% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" type="string" %}
Id of the wallet that will initiate the tx
{% endswagger-parameter %}

{% swagger-parameter in="body" name="to" type="string" %}
Destination Address (contract address)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="secretType" type="string" %}
On which blockchain the tx will be executed
{% endswagger-parameter %}

{% swagger-parameter in="body" name="value" type="integer" %}
Amount you want to transfer to
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactionRequest" type="object" %}
transactionRequest object
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```java
{
  "transactionHash" : "0x621f692e386a8bc0c53d36aa793864893106e10f54f63fa9c063e24ad975d907"
}
```
{% endswagger-response %}
{% endswagger %}

### Supported chain specific fields

| Property | Type    | Description                                                |
| -------- | ------- | ---------------------------------------------------------- |
| gasPrice | Integer | Gas price that will be used for the contract call (in WEI) |
| gasLimit | Integer | Gas limit that will be used for the contract call          |

### Supported types

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces ( ex: uint256\[] ). The values for an array must be surrounded with square brackets and delimited with "," (ex. \[1,2,3]). Byte values must be hex-encoded.

{% hint style="info" %}
🧙 The signatures endpoint supports the [EIP-712](https://eips.ethereum.org/EIPS/eip-712) standard, Ethereum typed structured data hashing and signing. This EIP aims to improve the usability of off-chain message signing for use on-chain.
{% endhint %}

## Example&#x20;

#### Request&#x20;

This example will execute an ERC20 transfer using the direct execution of the smart contract function "transfer". The inputs for this function are: destination (address) and amount (uint265)

```javascript
POST : https://api.arkane.network/api/transactions/execute
```

#### Request Body

```java
{
	"pincode": "1234",
	"transactionRequest": {

		"type": "CONTRACT_EXECUTION",
		"walletId": "adc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
		"to": "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
		"alias": null,
		"secretType": "ETHEREUM",
		"functionName": "transfer",
		"value": 0,
		"inputs": [{
			"type": "address",
			"value": "0x80cbb6c4342948e5be81987dce8251dbedd69138"
		}, {
			"type": "uint256",
			"value": 73680000
		}],
		"chainSpecificFields": {
			"gasLimit": "300000"
		}
	}
}
```

#### Response

```java
{
  "transactionHash" : "0x621f692e386a8bc0c53d36aa793864893106e10f54f63fa9c063e24ad975d907"
}
```

