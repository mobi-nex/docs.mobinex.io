---
sidebar_position: 2
---

# Installation

## From releases (Windows only)

You can download the latest release from [here](https://github.com/mobi-nex/adborc/releases).
The release contains all dependencies bundled, including `adb` and `scrcpy`.
Just extract the archive and run `adborc.exe` on the command line from the
extracted directory.

## Dependencies

Depending on the mode of operation, `AdbOrc` depends on the following:
1. [`adb`](https://developer.android.com/studio/releases/platform-tools) - Android Debug Bridge
2. [`scrcpy`](https://github.com/Genymobile/scrcpy) - *Optional*, for screen mirroring

For *MarketMaker* mode, none of the above are required.

For *Consumer* mode to work, minimum version of `adb` required is *1.0.41*.

Optionally, `scrcpy` can be used for screen mirroring. Minimum version of
`scrcpy` required is *1.13*.

For *Supplier* mode to work, minimum version of `adb` required is *1.0.41*, with
minimum revision number of *33.0.1*.

*Note:* `scrcpy` is not required for *Supplier* mode.

You can override the default `adb` and `scrcpy` used by:
```bash
# Full path to the adb executable
$ adborc set-adb-path <path_to_adb>

# Full path to the scrcpy executable
$ adborc set-scrcpy-path <path_to_scrcpy>
```

## From source

Installing `AdbOrc` from source requires the rust toolchain to be installed on your system.
Click [here](https://www.rust-lang.org/tools/install) for instructions on how to install the rust toolchain.

Assuming you have the rust toolchain installed:

```
$ cargo install --git https://github.com/mobi-nex/adborc.git 

# Or, if you want to build from local source
$ git clone https://github.com/mobi-nex/adborc.git
$ cd adborc

$ cargo install --path .
```

## From crates.io

If you have the rust toolchain installed, you can install `AdbOrc` from its published crate on
[crates.io](https://crates.io/crates/adborc):

```
$ cargo install adborc
```

*Note*: `AdbOrc` in *Consumer*/*Supplier* mode requires `adb` to be installed on the system. It also
requires `scrcpy` to be installed on the system if you wish to use
device screen mirroring. See [dependencies](#dependencies) section for more details. 
