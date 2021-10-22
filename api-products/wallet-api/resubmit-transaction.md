---
description: >-
  Sometimes a transaction fails to execute/propagate. This can be due to several
  factors, for example, the gas price is too low. Using this endpoint, you are
  able to resubmit an existing transaction.
---

# Resubmit transaction

{% swagger baseUrl="https://api.arkane.network" path="/api/transactions/resubmit" method="post" summary="Resubmit" %}
{% swagger-description %}
Safely resubmit a transaction. Executing this will overwrite the existing transaction.
{% endswagger-description %}

{% swagger-parameter in="body" name="secretType" type="string" %}
MATIC, BSC, ETHEREUM, ...
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactionHash" type="string" %}
Hash of the transaction to resubmit
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN associated with the wallet of the transaction
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "success": true,
    "result": {
        "transactionHash": "0xebe407f2b9987e1d37c371d395bdb603f5fc6eb43ac58711d77e7ed944b4261a"
    }
}
```
{% endswagger-response %}
{% endswagger %}

## Example

#### Request

```javascript
POST : https://api.arkane.network/api/transactions/resubmit
```

#### Request body

```javascript
{
    "secretType": "ETHEREUM",
    "transactionHash": "0x0e305bdf01149c2e35ea6ffb48ab474d714aa03173b06427c6325f0693c59f92",
    "pincode": "1234"
}
```

#### Response

```javascript
{
    "success": true,
    "result": {
        "transactionHash": "0xebe407f2b9987e1d37c371d395bdb603f5fc6eb43ac58711d77e7ed944b4261a"
    }
}
```
