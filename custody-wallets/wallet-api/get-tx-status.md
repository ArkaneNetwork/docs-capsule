---
description: >-
  Get the status of a specific transaction. Returns UNKNOWN when the specific
  chain is not supported yet.
---

# Get Tx status

{% api-method method="post" host="https://api.arkane.network" path="/api/transactions/<secretType>/<transactionHash>/status" %}
{% api-method-summary %}
Get the status of a transaction
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="transactionHash" type="string" required=true %}
The transaction hash \(id\)
{% endapi-method-parameter %}

{% api-method-parameter name="secretType" type="string" required=true %}
Chain \(Ethereum, MATIC, BSC,...\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```java
{
  "status" : "SUCCEEDED"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example 

#### Request 

```javascript
GET : https://api.arkane.network/api/transactions/ETHEREUM/0x4f2697187b720004d273e8ae67be50377a869622267595b1655d3c17af9452dc/status
```

#### Response

```java
{
  "status" : "SUCCEEDED"
}
```

