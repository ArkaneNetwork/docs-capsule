---
description: >-
  Sometimes a transaction fails to execute/propagate. This can be due to several
  factors, for example, the gas price is too low. Using this endpoint, you are
  able to resubmit an existing transaction.
---

# Resubmit transaction

{% api-method method="post" host="https://api.arkane.network" path="/api/transactions/resubmit" %}
{% api-method-summary %}
Resubmit
{% endapi-method-summary %}

{% api-method-description %}
Safely resubmit a transaction. Executing this will overwrite the existing transaction.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="secretType" type="string" required=true %}
MATIC, BSC, ETHEREUM, ...
{% endapi-method-parameter %}

{% api-method-parameter name="transactionHash" type="string" required=true %}
Hash of the transaction to resubmit
{% endapi-method-parameter %}

{% api-method-parameter name="pincode" type="string" required=true %}
PIN associated with the wallet of the transaction
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "result": {
        "transactionHash": "0xebe407f2b9987e1d37c371d395bdb603f5fc6eb43ac58711d77e7ed944b4261a"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

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

