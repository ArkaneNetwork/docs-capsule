# ExchangeTokenRequest

```java
{
    "clientId": "Arketype",
    "identityProvider": "FACEBOOK",
    "idpToken": "<remote_idp_token>"
}
```

| Field | Type | **Description** | Example |
| :--- | :--- | :--- | :--- |
| `clientId` | `string` | The client for which you want a token | `'Arketype'` |
| `identityProvider` | [`IdentityProvider`](identityprovider.md) | The identity provider to which the`idpToken` belongs | `'FACEBOOK'` |
| `idpToken` | `string` | The token of the external IDP |  |

