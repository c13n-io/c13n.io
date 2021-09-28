---
title: "Topics"
draft: false
type: "page"
weight: 1
image: "c13n-avatar.png"
---

## What is c13n

Sitting on top of Bitcoin & LightningNetwork layer, c13n is a component that makes your interaction with LN much easier. It acts as an intermediate layer between your application and your LN Node, without introducing any centralization characteristics.

c13n utilizes the node's interface to achieve a higher-level API, easy for devs to get used to and to start building on top of right away.

One of the main priorities of c13n is to be based as much as possible on Lightning Network communication (through micro-payments), and to utilize clearnet the least possible.


## How does it work

You can send payments and messages natively through c13n.

For the case of sending a simple message, the flow goes as follows:

- Your application will ask c13n to send a message to a specific discussion (involving one or more users).

- c13n will calculate which network route is optimal for the delivery of this payload.

- A composite message will be created, including routing info and a small fee for the the intermediate nodes routing your message.

- The intermediate nodes will receive this composite payload, acquire their micro fee, then deliver the message to the final node. During this routing process, intermediate nodes cannot read the content or any metadata related to the message sent to the final destination.

- The final destination retrieves the message.

## How is c13n deployed

c13n is technically a service, it exposes an API at a specific host and port, through which the communication with your application takes place. For ease of use it is recommended to run dockerized, as it will be much easier controlling and/or updating it.

### Requirements of c13n

The one and only requirement of c13n is a functional & reachable Lightning Network node (along with creds of course). Not all LN node implementations are supported, as of now, we have support for LND and partial support for C-Lightning.

## How to use c13n

After successfully deploying c13n on top of your node, you are ready to start building your application logic. For more information on how to use the c13n API check the [API Docs]().

There are no limitations on what you can build on top of c13n. You can build an end-user application that runs on a mobile device, or even a constantly running server that consumes the c13n API and exposes a new one.



## Our goal is to create a common baseline for Lightning Applications.
We want applications to have compatibility on the network layer as well as the application layer (for more info check [c13n-payload-protocol]()).

Making different chatting applications able to normally communicate with each other is a great milestone for this ecosystem. 

We envision an augmented ecosystem of services & apps over the Lightning Network, with easy integration and no compatibility friction.