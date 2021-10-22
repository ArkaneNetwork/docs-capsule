---
description: How to export an existing wallet
---

# Export a wallet

{% hint style="warning" %}
Please note that we do not export the private key, but rather a password secured keystore as it provides better protection against a man in the middle attack.&#x20;
{% endhint %}

{% swagger baseUrl="https://api.arkane.network" path="/api/wallets/{walletID}/export" method="post" summary="Export a wallet" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="walletId" type="string" %}
ID of the wallet you want to export
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pincode" type="string" %}
PIN to decrypt the wallet 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" type="string" %}
Password to secure the keystore
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "success": true,
    "result": {
        "keystore": "{\"address\":\"d7a742efa8f3b24bc39ef288c2eef3f1f6956a60\",\"id\":\"0c52bfce-0b64-4871-b6ff-30ef377a8fdd\",\"version\":3,\"crypto\":{\"cipher\":\"aes-128-ctr\",\"ciphertext\":\"1c1542c31c1ac5cab30a87d84a4091b150c508110859a8105a99c4cfc20357d3\",\"cipherparams\":{\"iv\":\"99ecb2a2fd5e9f081f9efdb8002b7a09\"},\"kdf\":\"scrypt\",\"kdfparams\":{\"dklen\":32,\"n\":262144,\"p\":1,\"r\":8,\"salt\":\"3646bcc831f00926890e4801cd741514846249ed5b1c79a6d2476b5cf4f4848c\"},\"mac\":\"bbbc32f0ebc35818459da82382cd44c6c16021da9e9bb62c7fc749f042cb4764\"}}"
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
For importing a wallet please have a look at[`import a wallet`](import-a-wallet.md).
{% endhint %}

## Example

#### Response

```javascript
{
    "success": true,
    "result": {
        "keystore": "{\"address\":\"d7a742efa8f3b24bc39ef288c2eef3f1f6956a60\",\"id\":\"0c52bfce-0b64-4871-b6ff-30ef377a8fdd\",\"version\":3,\"crypto\":{\"cipher\":\"aes-128-ctr\",\"ciphertext\":\"1c1542c31c1ac5cab30a87d84a4091b150c508110859a8105a99c4cfc20357d3\",\"cipherparams\":{\"iv\":\"99ecb2a2fd5e9f081f9efdb8002b7a09\"},\"kdf\":\"scrypt\",\"kdfparams\":{\"dklen\":32,\"n\":262144,\"p\":1,\"r\":8,\"salt\":\"3646bcc831f00926890e4801cd741514846249ed5b1c79a6d2476b5cf4f4848c\"},\"mac\":\"bbbc32f0ebc35818459da82382cd44c6c16021da9e9bb62c7fc749f042cb4764\"}}"
    }
}
```

