---
description: >-
  An endpoint to execute a function on a smart contract (write) on any
  (supported) blockchain. As a result, a new transaction will be submitted to
  the network containing the smart contract execution.
---

# Call a contract

{% api-method method="post" host="https://api.arkane.network" path="/api/transactions/execute" %}
{% api-method-summary %}
Call a contract
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="chainSpecificFields" type="object" required=true %}
Field that contains chain specific values,  see below.
{% endapi-method-parameter %}

{% api-method-parameter name="inputs.type" type="string" required=true %}
Type of the input parameter \(ex. uint256\)
{% endapi-method-parameter %}

{% api-method-parameter name="inputs.value" type="string" required=true %}
Value of the input parameter. This needs to be passed as a string value, will be parsed by Arkane
{% endapi-method-parameter %}

{% api-method-parameter name="inputs" type="array" required=true %}
Array of inputs needed to execute the function
{% endapi-method-parameter %}

{% api-method-parameter name="functionName" type="string" required=true %}
Contract function to call
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
PIN related to the wallet ID
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
CONTRACT\_EXECUTION
{% endapi-method-parameter %}

{% api-method-parameter name="walletId" type="string" required=true %}
Id of the wallet that will initiate the tx
{% endapi-method-parameter %}

{% api-method-parameter name="to" type="string" required=true %}
Destination Address \(can be a blockchain address or email address\)
{% endapi-method-parameter %}

{% api-method-parameter name="secretType" type="string" required=true %}
On which blockchain the tx will be executed
{% endapi-method-parameter %}

{% api-method-parameter name="value" type="integer" required=true %}
Amount you want to transfer to
{% endapi-method-parameter %}

{% api-method-parameter name="transactionRequest" type="object" required=true %}
transactionRequest object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```java
{
  "transactionHash" : "0x621f692e386a8bc0c53d36aa793864893106e10f54f63fa9c063e24ad975d907"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Supported chain specific fields

| Property | Type | Description |
| :--- | :--- | :--- |
| gasPrice | Integer | Gas price that will be used for the contract call \(in WEI\) |
| gasLimit | Integer | Gas limit that will be used for the contract call |

### Supported types

`address, bool, bytes, bytes1, bytes2, bytes3, bytes4, bytes5, bytes6, bytes7, bytes8, bytes9, bytes10, bytes11, bytes12, bytes13, bytes14, bytes15, bytes16, bytes17, bytes18, bytes19, bytes20, bytes21, bytes22, bytes23, bytes24, bytes25, bytes26, bytes27, bytes28, bytes29, bytes30, bytes31, bytes32, int8, int16, int24, int32, int40, int48, int56, int64, int72, int80, int88, int96, int104, int112, int120, int128, int136, int144, int152, int160, int168, int176, int184, int192, int200, int208, int216, int224, int232, int240, int248, int256, string, uint8, uint16, uint24, uint32, uint40, uint48, uint56, uint64, uint72, uint80, uint88, uint96, uint104, uint112, uint120, uint128, uint136, uint144, uint152, uint160, uint168, uint176, uint184, uint192, uint200, uint208, uint216, uint224, uint232, uint240, uint248, uint256`

For arrays, please provide the type from above followed by square braces \( ex: uint256\[\] \). The values for an array must be surrounded with square brackets and delimited with "," \(ex. \[1,2,3\]\). Byte values must be hex-encoded.

{% hint style="info" %}
🧙 The signatures endpoint supports the [EIP-712](https://eips.ethereum.org/EIPS/eip-712) standard, Ethereum typed structured data hashing and signing. This EIP aims to improve the usability of off-chain message signing for use on-chain.
{% endhint %}

## Example 

#### Request 

This example will execute an ERC20 transfer using the direct execution of the smart contract function "transfer". The inputs for this function are: destination \(address\) and amount \(uint265\)

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



