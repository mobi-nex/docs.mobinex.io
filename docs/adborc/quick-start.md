---
sidebar_position: 3
---

# Quick Start

## Start Network

Start the network by starting *MarketMaker* on a machine:

```bash
$ adborc marketmaker start
```

## Supply Devices 

To supply devices to the network, join the network as a *Supplier*.
This can be done from the same computer as the *MarketMaker* or from any another computer that has the devices connected to it.
All communication between the *MarketMaker*, *Supplier* and *Consumer* is encrypted and authenticated. But by default, the
device communications over adb are not encrypted. To enable encryption, use the `--secure` flag when starting the *Supplier*.
This will enable encrypted tunnels for all devices that are supplied by the *Supplier*. To join the network as a *Supplier*:  

```bash
$ adborc supplier start <MarketMaker_IP/HostName>

# Or, if you wish to enable secure mode
$ adborc supplier start <MarketMaker_IP/HostName> --secure

# Supply specific devices to the network
$ adborc supplier supply --devices "<android_serial1>,<android_serial2>,..."

# Or, supply all connected devices
$ adborc supplier supply
```

## Use Devices

To use devices from the network, join the network as a *Consumer*. This can be done from the same computer as the *MarketMaker*
or from any another computer. To join the network as a *Consumer*:

```bash
$ adborc consumer start <MarketMaker_IP/HostName>

# List available devices
$ adborc consumer list-available

# Reserve devices
$ adborc consumer reserve <device_id>

# Use the devices via adb
$ adb shell

# Or, use the devices via scrcpy
$ adborc consumer scrcpy <device_id>
```
