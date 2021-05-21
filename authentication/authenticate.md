---
description: How to get a Bearer token
---

# How to get a Bearer token

{% api-method method="post" host="https://login.arkane.network" path="/auth/realms/Arkane/protocol/openid-connect/token" %}
{% api-method-summary %}
Get bearer and refresh token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="grant\_type" type="string" required=true %}
client\_credentials
{% endapi-method-parameter %}

{% api-method-parameter name="client\_id" type="string" required=true %}
Private client id
{% endapi-method-parameter %}

{% api-method-parameter name="client\_secret" type="string" required=true %}
Secret
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Status of the call and the wallet is returned.
{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "eyJhbGciOsJSUzI1NiIsInR3cCIgOiAiSldUIiwia2lkIiA6ICJmQi1UenBOb0hBVGhwT2J4aW9qTDBrdm83MldmRzRXRXh1eFpiaXlGQUhzIn0.eyJleHAiOjE2MTI5MDYwNTksImlhdCI6MTYxMjkwNDI1OSwianRpIjoiYWVkYjFlMGYtOGE1Yi00ZjRiLWEwMTQtMDQyNmJiOGZkN2JkIiwiaXNzIjoiaHR0cHM6Ly9sb2dpbi1xYS5hcmthbmUubmV0d29yay9hdXRoL3JlYWxtcy9BcmthbmUiLCJhdWQiOiJyZWFsbS1tYW5hZ2VtZW50Iiwic3ViIjoiNDkxN2I2ZmEtMjY1Ny00YmRkLWI4ZTgtZmE1ZGQ4YmQ0MDU3IiwidHlwIjoiQmVhcmVyIiwiYXpwIjoiU3RyaWVnZWwtY2Fwc3VsZSIsInNlc3Npb25fc3RhdGUiOiI4NWJhZWY0ZS1hZDZjLTQ4ZDAtYTQ3Yy1mNWYxNzQ0OTI0ZWMiLCJhY3IiOiIxIiwicmVzb3VyY2VfYWNjZXNzIjp7InJlYWxtLW1hbmFnZW1lbnQiOnsicm9sZXMiOlsicXVlcnktY2xpZW50cyIsInF1ZXJ5LWdyb3VwcyJdfX0sInNjb3BlIjoidmlldzp3YWxsZXRzIHVzZTphbGwtd2FsbGV0cyB3aGl0ZWxhYmVsIHNpZ246d2FsbGV0cyB2aWV3OnByb2ZpbGUgc2F2ZTp0cmFuc2FjdGlvbiBlbWFpbCBwcm9maWxlIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJjbGllbnRIb3N0IjoiMTcyLjY5LjU0LjM1IiwiY2xpZW50SWQiOiJTdHJpZWdlbC1jYXBzdWxlIiwicHJlZmVycmVkX3VzZXJuYW1lIjoic2VydmljZS1hY2NvdW50LXN0cmllZ2VsLWNhcHN1bGUiLCJjbGllbnRBZGRyZXNzIjoiMTcyLjY5LjU0LjM1In0.dWxl4rUWMkpfNXLXvoV5eHuGwlyZZu-czjZj8be6ssvK2oq-ZrBxh-gBWCZAqIcKE_dQXKQYBFSlViB2DI-_gCeApaacXiECDr9LdEoPeOe9DU0rzxX2a8diK6XzaS_GOBNt32b79ZYatWzWA2J1tyBZbGvairmyW1FldHi4NQvQyn4UDK-rhLG0RapGQyFSiD0cmXHf765uTasXP9cAa7NNyihpdcVcTjVfdAJGW-I2D7QrjyQZBdx_HqKTafheKhlv-OLnldILxsOIfOI6FTAX9zItHkBRCSL7KhnkLA0jjzHviCefxsu3qItelyK9bkf6pFjkiqqJBE9VETM2Qg",
    "expires_in": 1800,
    "refresh_expires_in": 3456000,
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJlOTVlMDc2NC1lZmVkLTQyMmEtYmU0Mi1iZTcwYmY1Nzg2NDYifQ.eyJleHAiOjE2MTYzNjAyNTksImlhdCI6MTYxMjkwNDI1OSwianRpIjoiZTFiNGM5ZDQtYTI5YS00MDJmLWFiNjMtYzZlOTdjZWJjNWY3IiwiaXNzIjoiaHR0cHM6Ly9sb2dpbi1xYS5hcmthbmUubmV0d29yay9hdXRoL3JlYWxtcy9BcmthbmUiLCJhdWQiOiJodHRwczovL2xvZ2luLXFhLmFya2FuZS5uZXR3b3JrL2F1dGgvcmVhbG1zL0Fya2FuZSIsInN1YiI6IjQ5MTdiNmZhLTI2NTctNGJkZC1iOGU4LWZhNWRkOGJkNDA1NyIsInR5cCI6IlJlZnJlc2giLCJhenAiOiJTdHJpZWdlbC1jYXBzdWxlIiwic2Vzc2lvbl9zdGF0ZSI6Ijg1YmFlZjRlLWFkNmMtNDhkMC1hNDdjLWY1ZjE3NDQ5MjRlYyIsInNjb3BlIjoidmlldzp3YWxsZXRzIHVzZTphbGwtd2FsbGV0cyB3aGl0ZWxhYmVsIHNpZ246d2FsbGV0cyB2aWV3OnByb2ZpbGUgc2F2ZTp0cmFuc2FjdGlvbiBlbWFpbCBwcm9maWxlIn0.NbqHUU56DbGCdD0ZVCTiKo440ZzJ1bORGxuSEATvvLM",
    "token_type": "bearer",
    "not-before-policy": 1572970662,
    "session_state": "85baef4e-ad6c-48d0-a47c-f5f1744924ec",
    "scope": "view:wallets use:all-wallets whitelabel sign:wallets view:profile save:transaction email profile"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example

#### Request

![](../.gitbook/assets/image%20%282%29.png)

#### Response

```javascript
{
    "access_token": "eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJmQi1UenBOb0hBVGhwT2J4aW9qTDBrdm83MldmRzRXRXh1eFpiaXlGQUhzIn0.eyJleHAiOjE2MTI5MDYwNTksImlhdCI6MTYxMjkwNDI1OSwianRpIjoiYWVkYjFlMGYtOGE1Yi00ZjRiLWEwMTQtMDQyNmJiOGZkN2JkIiwiaXNzIjoiaHR0cHM6Ly9sb2dpbi1xYS5hcmthbmUubmV0d29yay9hdXRoL3JlYWxtcy9BcmthbmUiLCJhdWQiOiJyZWFsbS1tYW5hZ2VtZW50Iiwic3ViIjoiNDkxN2I2ZmEtMjY1Ny00YmRkLWI4ZTgtZmE1ZGQ4YmQ0MDU3IiwidHlwIjoiQmVhcmVyIiwiYXpwIjoiU3RyaWVnZWwtY2Fwc3VsZSIsInNlc3Npb25fc3RhdGUiOiI4NWJhZWY0ZS1hZDZjLTQ4ZDAtYTQ3Yy1mNWYxNzQ0OTI0ZWMiLCJhY3IiOiIxIiwicmVzb3VyY2VfYWNjZXNzIjp7InJlYWxtLW1hbmFnZW1lbnQiOnsicm9sZXMiOlsicXVlcnktY2xpZW50cyIsInF1ZXJ5LWdyb3VwcyJdfX0sInNjb3BlIjoidmlldzp3YWxsZXRzIHVzZTphbGwtd2FsbGV0cyB3aGl0ZWxhYmVsIHNpZ246d2FsbGV0cyB2aWV3OnByb2ZpbGUgc2F2ZTp0cmFuc2FjdGlvbiBlbWFpbCBwcm9maWxlIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJjbGllbnRIb3N0IjoiMTcyLjY5LjU0LjM1IiwiY2xpZW50SWQiOiJTdHJpZWdlbC1jYXBzdWxlIiwicHJlZmVycmVkX3VzZXJuYW1lIjoic2VydmljZS1hY2NvdW50LXN0cmllZ2VsLWNhcHN1bGUiLCJjbGllbnRBZGRyZXNzIjoiMTcyLjY5LjU0LjM1In0.dWxl4rUWMkpfNXLXvoV5eHuGwlyZZu-czjZj8be6ssvK2oq-ZrBxh-gBWCZAqIcKE_dQXKQYBFSlViB2DI-_gCeApaacXiECDr9LdEoPeOe9DU0rzxX2a8diK6XzaS_GOBNt32b79ZYatWzWA2J1tyBZbGvairmyW1FldHi4NQvQyn4UDK-rhLG0RapGQyFSiD0cmXHf765uTasXP9cAa7NNyihpdcVcTjVfdAJGW-I2D7QrjyQZBdx_HqKTafheKhlv-OLnldILxsOIfOI6FTAX9zItHkBRCSL7KhnkLA0jjzHviCefxsu3qItelyK9bkf6pFjkiqqJBE9VETM2Qg",
    "expires_in": 1800,
    "refresh_expires_in": 3456000,
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJlOTVlMDc2NC1lZmVkLTQyMmEtYmU0Mi1iZTcwYmY1Nzg2NDYifQ.eyJleHAiOjE2MTYzNjAyNTksImlhdCI6MTYxMjkwNDI1OSwianRpIjoiZTFiNGM5ZDQtYTI5YS00MDJmLWFiNjMtYzZlOTdjZWJjNWY3IiwiaXNzIjoiaHR0cHM6Ly9sb2dpbi1xYS5hcmthbmUubmV0d29yay9hdXRoL3JlYWxtcy9BcmthbmUiLCJhdWQiOiJodHRwczovL2xvZ2luLXFhLmFya2FuZS5uZXR3b3JrL2F1dGgvcmVhbG1zL0Fya2FuZSIsInN1YiI6IjQ5MTdiNmZhLTI2NTctNGJkZC1iOGU4LWZhNWRkOGJkNDA1NyIsInR5cCI6IlJlZnJlc2giLCJhenAiOiJTdHJpZWdlbC1jYXBzdWxlIiwic2Vzc2lvbl9zdGF0ZSI6Ijg1YmFlZjRlLWFkNmMtNDhkMC1hNDdjLWY1ZjE3NDQ5MjRlYyIsInNjb3BlIjoidmlldzp3YWxsZXRzIHVzZTphbGwtd2FsbGV0cyB3aGl0ZWxhYmVsIHNpZ246d2FsbGV0cyB2aWV3OnByb2ZpbGUgc2F2ZTp0cmFuc2FjdGlvbiBlbWFpbCBwcm9maWxlIn0.NbqHUU56DbGCdD0ZVCTiKo440ZzJ1bORGxuSEATvvLM",
    "token_type": "bearer",
    "not-before-policy": 1572970662,
    "session_state": "85baef4e-ad6c-48d0-a47c-f5f1744924ec",
    "scope": "view:wallets use:all-wallets whitelabel sign:wallets view:profile save:transaction email profile"
}
```



