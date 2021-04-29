---
description: How to access Arkane API
---

# Authentication

## Client ID

To connect to our [staging or production environment](../deep-dive/environments-and-networks.md) and the different networks, a private Client ID is required. By using a Client ID that is linked to your application, an extra level of security is added, as it allows transaction filtering based on origin. 

{% hint style="info" %}
🧙 To connect to our environments, please [fill in this form](https://get.arkane.network/) to contact us.
{% endhint %}

## Basic Authentication flow

A client id comes with a `shared secret` that can be used to retrieve a `Bearer token` which can be used to call the different endpoints. Here is a small diagram explain the authentication flow.

![Basic Authentication flow](../.gitbook/assets/image%20%288%29%20%281%29.png)

{% hint style="info" %}
The authentication flow requires a server -to-server communication channel 
{% endhint %}

