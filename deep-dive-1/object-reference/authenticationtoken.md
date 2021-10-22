# AuthenticationToken

```java
{
    "access_token": "<access_token>",
    "expires_in": 1800,
    "refresh_expires_in": 3456000,
    "refresh_token": "<refresh_token>",
    "token_type": "bearer",
    "scope": "view:wallets sign:wallets view:profile email profile"
}
```

| Parameter            | type     | **Description**                                                  | Example                                                                           |
| -------------------- | -------- | ---------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `access_token`       | `string` | Access token that allows access to the resource                  | `'https://foo.io'`                                                                |
| `expires_in`         | `number` | How long the `access_token` is valid                             | `1800`                                                                            |
| `refresh_expires_in` | `string` | How long the `refresh_token` is valid                            | `false`                                                                           |
| `refresh_token`      | `string` | The refresh token that can be used to request a new access token | <p><code>google</code></p><p><code>facebook</code></p><p><code>twitter</code></p> |
| `token_type`         | `string` | The type for the token, will be "bearer"                         | `'bearer'`                                                                        |
| `scope`              | `string` | The scopes for this token                                        |                                                                                   |
