---
layout: layouts/post.njk
title: How do I make sneaker monitor?
description: Monitors are really cool but how do I make one?
date: 2021-10-01T21:00:00.000Z
featuredImage: /images/uploads/sneaker-bots.jpeg
---
# Ok but what in the world is a monitor?

a monitor in this instance is not a PC monitor in this scenario a monitor is an application that notifies you when a new product drops or restocks in a certain site (eg. supreme, yeezysupply, footsites, etc.) usually a monitor notifies you via discord webhooks.

## Alright but how do I make a monitor?

This will be the topic of this exact article, 

We'll be making a supreme monitor

Some things we'll before starting will be:

Node.js (LTS version as of writing this article it is 14.18.0)

Code editor (we'll be using VSCode)

Some basic understanding of Node.js



Alright let's get started:

First we'll start our project by running `npm init` and then we'll create a folder named `index.js` and then run `npm i node-fetch discord-webhook-node` to install our dependances and then inside of our `index.js` file we'll write for our base code:

```javascript
import fetch from 'node-fetch';
import { Webhook, MessageBuilder } from 'discord-webhook-node';
```

This code does nothing at all by it self lets spice it up by adding:

```javascript
async function DoAtOnce {
setTimeout(() => {
 const IntialData = await fetch('https://www.supremenewyork.com/mobile_stock.json').then((res => res.json()))
}, 2000)
}
```