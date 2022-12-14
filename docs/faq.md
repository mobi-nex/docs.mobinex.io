---
slug: /faq
sidebar_position: 5
---

# Frequently Asked Questions

### Can *Supplier* and *Consumer* be started on the same machine?

Yes, Supplier and Consumer can be started on the same machine. In fact, Supplier, Consumer and MarketMaker can all be started on the same machine.

:::note

If MarketMaker is started on a machine, Supplier and Consumer can only be started on the same machine if they are connected to the local MarketMaker.

:::

### Can I use a device that is reserved by another user?

No, you cannot use a device that is reserved by another user. You can only use a device that is reserved by you. Two users cannot reserve the same device at the same time.
If you are the Supplier of the device, you can use `adb` to connect to the device even if it is reserved by another user, but the device will not be available
on the default `adb` port. You can use the `adborc supplier status` command to get the port on which the device is internally available.

### Are there any test frameworks integrated with MobiNex?

At the moment, there are no test frameworks integrated with MobiNex. However, you can use any test framework that uses `adb` to run tests on devices.
If you have any suggestions for test frameworks that you would like to see integrated with MobiNex, please let us know on [GitHub](https://github.com/mobinex/adborc/issues).
Any contributions are welcome!

### Can I use MobiNex with a device that is not connected to the internet?

Yes, you can use MobiNex with a device that is not connected to the internet. Only requirement is that the device is connected to a Supplier machine via USB
and detected by `adb`.

### Is wireless `adb` supported?

No, wireless `adb` is not supported at the moment. Currently, MobiNex only supports USB connection for devices.

