---
sidebar_position: 2
title: Device Supply Issues
draft: true
---

# Device Supply Issues

Some common issues with device supply are listed below:

:::note

If you are facing any other issues, please report the issue on [GitHub](https://github.com/mobi-nex/adborc/issues).

:::

## Devices not showing up on `adb` after stopping *Supplier*

If you have stopped Supplier mode and your devices are not showing up in adb, try to kill all adb servers on your system.
If you are on windows, you can look for the `adb` process in the task manager and kill it or, you can use the following command:

```bash
taskkill /F /IM adb.exe
```

If you are on linux, you can use the following command:

```bash
killall adb
```

If you are on mac, you can use the following command:

```bash
killall adb
```
