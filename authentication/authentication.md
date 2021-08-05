---
description: How to access Venly API
---

# How to authenticate

## Client ID & Secret

To connect to our [staging or production environment](../advanced/environments-and-networks.md) and the different networks, a private Client ID is required. By using a Client ID that is linked to your application, an extra level of security is added, as it allows transaction filtering based on origin. 

{% hint style="info" %}
🧙 To connect to our systems, please request access using [this form](https://forms.venly.io/clientID). 
{% endhint %}

## Already have your Client ID & Secret?

Awesome, no time to waste, full speed ahead. 

The best place to start is by downloading our [Postman Collection](https://documenter.getpostman.com/view/11995086/TzXwEdfX). It covers all our available endpoints for all our API products. Once downloaded you only need to update the variables with your own client id and secret and you are good to go.

![](../.gitbook/assets/image%20%2821%29.png)

{% hint style="info" %}
By default our postman collection points to our staging environment, which is connected to different testnets and is the perfect environment to start playing around. To learn more about our environments and the different blockchain networks please have a look at [Environments & networks](../advanced/environments-and-networks.md).
{% endhint %}

## Basic Authentication flow

A client id comes with a `shared secret` that can be used to retrieve a `Bearer token` which can be used to call the different endpoints. Here is a small diagram explain the authentication flow.

![Basic Authentication flow](../.gitbook/assets/image%20%288%29%20%281%29.png)

{% hint style="info" %}
The authentication flow requires a server-to-server communication channel 
{% endhint %}

