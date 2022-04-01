---
title: "About"
draft: false
type: "page"
weight: 1
image: "c13n-avatar.png"
---

> **c13n** - Creating a common baseline for Lightning Applications

## What is c13n

> Pronounced "c-thirteen"

Sitting on top of Lightning Network layer, c13n is a component that introduces new ways to use Lightning. It acts as an intermediate layer over your LN node, enabling ⚡data transfer over lightning⚡ for applications!

c13n utilizes the node's interface to achieve a higher-level API, including both payment and data focused features, easy for devs to get used to and to start building on top of right away.

One of the main priorities of c13n is to be based exclusively on Lightning micro-payments and to not utilize clearnet.

![](/arch_overview.png)


## How does it work

### Stack

c13n is a communication oriented abstraction layer over the RPC API provided by [lnd](https://github.com/lightningnetwork/lnd/). LND is the Lightning node implementation of choice so far, while support for additional implementations will be implemented in the future.

You can deploy c13n in front of your Lightning node and enable data transfer capabilities, without introducing unwanted side-effects to your Lightning node. By doing so, you are now able to not only send payments to any node in the network, but also data! Every message/payment sent over c13n is a payment over Lightning, and you are able to inspect it with any other tool/dashboard.

The c13n abstraction layer is provided as a RPC API ready to be consumed for your next-gen Lightning app!


### Messages are Payments

Every message sent with c13n is actually a Lightning payment. This means that there is a price for each message, averaging around 2-3 satoshis (merely 0.1 pennies), which is used as a fee to intermediate nodes who forward your payload.

A single message cannot be greater than ~1KB in size. This limit is dynamic as it depends on multiple factors, one being the length of the route of the payment carrying the message.


### Why over Lightning

Because at the price of a few sats you get:

- A unified payment & data medium, leading to simplified architectures for apps and services.
- Data inherit the security & privacy model of Lightning payments.
- Participants in the network are public keys, facilitating data authentication with their signatures.
- No need for new configurations on already existing setups, as all c13n does is utilize the Lightning node.


## Why c13n
Developing and releasing Lightning Applications becomes a matter of setting up c13n and utilizing the c13n shipped API.

Developers can now realize innovative applications, focusing on the bigger picture avoiding spending vast amounts of time on gaining LN expertise.

We promote compatibility of data on both Lightning layer (how data is carried over payments) and application layer (payload specs for applications). Making applications and services able to normally communicate with each other is a great starting point for this ecosystem.

We envision an augmented ecosystem of services & apps over the Lightning Network, with easy bootstrapping, deployment, integration and interoperability.