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

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">type</th>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>access_token</code>
      </td>
      <td style="text-align:left"><code>string</code>
      </td>
      <td style="text-align:left">Access token that allows access to the resource</td>
      <td style="text-align:left"><code>&apos;https://foo.io&apos;</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>expires_in</code>
      </td>
      <td style="text-align:left"><code>number</code>
      </td>
      <td style="text-align:left">How long the <code>access_token</code> is valid</td>
      <td style="text-align:left"><code>1800</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>refresh_expires_in</code>
      </td>
      <td style="text-align:left"><code>string</code>
      </td>
      <td style="text-align:left">How long the <code>refresh_token</code> is valid</td>
      <td style="text-align:left"><code>false</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>refresh_token</code>
      </td>
      <td style="text-align:left"><code>string</code>
      </td>
      <td style="text-align:left">The refresh token that can be used to request a new access token</td>
      <td
      style="text-align:left">
        <p><code>google</code>
        </p>
        <p><code>facebook</code>
        </p>
        <p><code>twitter</code>
        </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>token_type</code>
      </td>
      <td style="text-align:left"><code>string</code>
      </td>
      <td style="text-align:left">The type for the token, will be &quot;bearer&quot;</td>
      <td style="text-align:left"><code>&apos;bearer&apos;</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>scope</code>
      </td>
      <td style="text-align:left"><code>string</code>
      </td>
      <td style="text-align:left">The scopes for this token</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

