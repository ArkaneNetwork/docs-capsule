---
description: >-
  This page describes how the authentication bridge can be used. This allows you
  to swap an Identity Provider Token (IDP) for a Venly authentication token.
---

# Authentication Bridge

{% swagger baseUrl="https://connect.arkane.network" path="/auth/exchange" method="post" summary="Exchange token" %}
{% swagger-description %}
This endpoint allows you to exchange authentication tokens
{% endswagger-description %}

{% swagger-parameter in="header" name="content-type" type="string" %}
application/json
{% endswagger-parameter %}

{% swagger-parameter in="body" name="clientId" type="string" %}
The client id for which you want a token (Ex. Arketype)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="identityProvider" type="object" %}
Which IdentityProvider to use
{% endswagger-parameter %}

{% swagger-parameter in="body" name="idpToken" type="string" %}
The token of the external IDP
{% endswagger-parameter %}

{% swagger-response status="200" description="Returns AuthenticationToken" %}
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
{% endswagger-response %}
{% endswagger %}

```
{
    "clientId": "Arketype",
    "identityProvider": "FACEBOOK",
    "idpToken": "<facebook_access_token"
}
```

