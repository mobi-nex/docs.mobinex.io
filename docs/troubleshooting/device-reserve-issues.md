---
sidebar_position: 1
title: Device Reservation Issues
draft: true
---

# Issues with Device Reservation

Some common issues with device reservation are listed below:

:::note

If you are facing any other issues, please report the issue on [GitHub](https://github.com/mobi-nex/adborc/issues).

:::

## Reserved devices not showing up on *Consumer* `adb`

If the devices are reserved successfully but not showing up on `adb`, on the *Supplier* side, please check
if any firewall is blocking the `adb` process.

Alternatively, try restarting the *Supplier* in secure mode and then reserve the device again.