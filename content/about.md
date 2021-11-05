---
title: "About"
draft: false
type: "page"
weight: 1
image: "c13n-avatar.png"
---

> **c13n** - Creating a common baseline for Lightning Applications ⚡

## What is c13n

> Pronounced "c-thirteen"

Sitting on top of Bitcoin & Lightning Network layer, c13n is a component that makes your interaction with LN much easier. It acts as an intermediate layer between your application and your LN Node, without introducing any centralization characteristics.

c13n utilizes the node's interface to achieve a higher-level API, easy for devs to get used to and to start building on top of right away.

One of the main priorities of c13n is to be based as much as possible on Lightning Network communication (through micro-payments), and to utilize clearnet the least possible.

![](/arch_overview.png)


## How does it work

### Stack

c13n is a communication oriented abstraction layer over the RPC API provided by [lnd](https://github.com/lightningnetwork/lnd/). LND is the lightning node implementation of choice so far, while support for additional implementations will be implemented in the future.

Lightning network is a layer operating on top of Bitcoin, hence the c13n stack basis is a bitcoin daemon.

The c13n abstraction layer is provided as a RPC API ready to be consumed for your next Lightning app!

### Sending a message/payment

- Your application will ask c13n to send a message/payment to a specific discussion (involving one or more users).

- Utilizing node route calculation features, c13n will use the optimal LN route.

- A composite message will be created, including routing info and a small fee for the the intermediate nodes routing your message/payment.

- Intermediate nodes will receive this composite payload, acquire their micro fee, then deliver the message to the final node. During this routing process, intermediate nodes cannot read the content or any metadata related to the message sent to the final destination.

- The final destination retrieves the message.


## Why c13n
Developing and releasing Lightning Applications becomes a matter of setting up the c13n stack and utilizing the c13n shipped API.

Developers can now realize innovative applications, focusing on the bigger picture avoiding spending vast amounts of time on gaining LN expertise.

We want applications to have compatibility on the network layer as well as the application layer. Making chatting applications and services able to normally communicate with each other is a great milestone for this ecosystem.

We envision an augmented ecosystem of services & apps over the Lightning Network, with easy bootstrapping, deployment, integration and interoperability.