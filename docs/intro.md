---
slug: /
sidebar_position: 1
---

# Overview


## What is MobiNex?

*MobiNex* is a platform that allows you to easily create a pseudo-distributed network of android devices and
share them with other users on the network. It can be used for setting up remote testing and development
environments for your engineering team. It can also be used for setting up an in-house testing farm or
a [virtual device lab](https://mobinex.io/blog/why-setup-a-virtual-device-lab) for your organization.


## How does it work?

A MobiNex network consists of one or more *Suppliers* and one or more *Consumers*. A Supplier node is a
computer on the network that has one or more android devices attached to it. A Consumer node is a computer
on the network that wants to use these supplied devices. This simple supplier-consumer model allows you
to easily scale your network to any size and reduces the complexity of managing the devices while being
fault tolerant to node failures and highly available.

## What does pseudo-distributed mean?

In a MobiNex network, the devices are connected to *Supplier* nodes via USB. The Supplier nodes are
connected to *Consumer* nodes via the *network*. When a Consumer wants to use a device, it *connects* to
the Supplier that has the device attached to it. All device communication, after the connection, is
completely distributed and peer-to-peer between the Consumer and the Supplier. In addition to
Supplier and Consumer nodes, there is a central *MarketMaker* node that manages the network and acts
as a proxy for the network. MarketMaker is responsible for the connection between Supplier and
Consumer. It also handles all the metadata of the network. This means that the network is fault
tolerant to Supplier and Consumer node failures, but it is not fault tolerant to MarketMaker node failure.

## How do I get started?

The MobiNex platform consists of two tools for setting up and managing the network:

1. [SwapMeet](/category/swapmeet-gui) - A desktop application for setting up and managing the network.
2. [AdbOrc](/category/adborc-cli) - A command line tool for managing the network.

You can use either of these tools to set up and manage your network. *SwapMeet* is recommended for
setting up the network for the first time because it provides a simple and intuitive UI for managing
the network. For advanced users, *AdbOrc* can be used to manage the network from the command line.
It is also possible to use both tools together. AdbOrc is also the core of MobiNex
and used by SwapMeet internally to manage the network. AdbOrc is open source and the source code is
available on [GitHub](https://github.com/mobi-nex/adborc.git).


:::tip

Installing SwapMeet will also install AdbOrc on your system.

:::