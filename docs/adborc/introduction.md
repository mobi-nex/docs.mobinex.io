---
sidebar_position: 1
---

# Introduction

`AdbOrc` is a tool that makes it easy to create a psuedo-distributed network of Android devices for testing and development purposes.
It is a simple wrapper around the `adb` command line tool that allows you to easily share devices with other users on the network.

## Overview

There are three modes of operation for a network node in `AdbOrc`:

1. *Supplier* - A machine on the network that has one or more android
    devices attached to it. *Supplier*, as the name implies, supplies
    devices to the network. There can be any number of *Supplier*s on
    the network.

2. *Consumer* - A machine on the network that wants to use one or more
    android devices. *Consumer*, as the name implies, consumes devices
    from the network. There can be any number of *Consumer*s on the
    network.

3. *MarketMaker* - A machine on the network that acts as a middleman
    between *Supplier*s and *Consumer*s. MarketMaker is responsible
    for matching Suppliers and Consumers and handling all the metadata
    of the network. There is exactly one *MarketMaker* on the network.
    For Suppliers and Consumers, MarketMaker serves as a proxy
    for the network.

A system on the network can be operating in any combination of the
above modes. For example, a system can be a *Supplier* and a *Consumer*
at the same time. It can also be a *MarketMaker* and a *Consumer* at
the same time.

Supplying devices to the network is as simple as joining the network
as a *Supplier* and choosing the devices you wish to supply.

To use devices from the network, you need to join the network as a
*Consumer* and list the available devices within the network.
You can then choose the devices you wish to use and ask *MarketMaker*
to reserve them for you. Once you are done using the devices, you can
release them back to the network.

All reserved devices are available for use only to the *Consumer* that
reserved them. The devices are available directly via `adb`. Device
screen mirroring for reserved devices is also supported directly by
`AdbOrc` via [`scrcpy`](https://github.com/Genymobile/scrcpy).
