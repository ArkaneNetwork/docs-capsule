---
description: >-
  This page describes how the authentication bridge can be used. This allows you
  to swap an Identity Provider Token (IDP) for a Venly authentication token.
---

# Authentication Bridge

{% api-method method="post" host="https://connect.arkane.network" path="/auth/exchange" %}
{% api-method-summary %}
Exchange token
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to exchange authentication tokens
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="clientId" type="string" required=true %}
The client id for which you want a token \(Ex. Arketype\)
{% endapi-method-parameter %}

{% api-method-parameter name="identityProvider" type="object" required=true %}
Which IdentityProvider to use
{% endapi-method-parameter %}

{% api-method-parameter name="idpToken" type="string" required=true %}
The token of the external IDP
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns AuthenticationToken
{% endapi-method-response-example-description %}

```
{
    "access_token": "<generated_access_token>",
    "expires_in": 1800,
    "refresh_expires_in": 3456000,
    "refresh_token": "<generated_refresh_token>",
    "token_type": "bearer",
    "not-before-policy": 1572970662,
    "session_state": "ed089e20-43ff-4990-812e-74fb2b897403",
    "scope": "view:wallets sign:wallets view:profile email profile"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
{
    "clientId": "Arketype",
    "identityProvider": "FACEBOOK",
    "idpToken": "<facebook_access_token"
}
```



