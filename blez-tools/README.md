BLEZ tools -- swiss army knife for GATT services and L2CAP sockets on Linux
===========================================================================

[![crates.io page](https://img.shields.io/crates/v/blez-tools)](https://crates.io/crates/blez-tools)
[![BSD-2-Clause license](https://img.shields.io/crates/l/blez-tools)](https://github.com/surban/blez/blob/master/LICENSE)

## Renamed to BlueR

blez-tools has been renamed to [bluer-tools](https://crates.io/crates/bluer-tools).

Development will continue in the [BlueZ organization repository](https://github.com/bluez/bluer).

Please update your links and crate references.

---

This crate provides tools for [Bluetooth Low Energy (BLE)](https://en.wikipedia.org/wiki/Bluetooth_Low_Energy) on Linux,
building on the functionality of the [BLEZ library](https://crates.io/crates/blez).

The following command line tools are included.

  - **blemon**: Scans for and monitors Bluetooth LE devices similar to `top`.

  - **gattcat**: Swiss army knife for Bluetooth LE GATT services.
    - discovers Bluetooth LE devices and their services
    - pairing
    - resolves all well-known UUIDs and manufacturer ids
    - performs all possible operations on GATT services
    - connects (via notify and write) to a remote GATT service
    - serves (via notify and write) a local program over a GATT service
    - implements the [Nordic UART service (NUS)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/include/bluetooth/services/nus.html) as client and server

  - **l2cat**: [netcat](https://sectools.org/tool/netcat/)-like for Bluetooth LE L2CAP sockets.
    - connects to remote L2CAP PSMs
    - listens on local L2CAP PSMs and accepts connections
    - serves a local program on an L2CAP PSM

Each tool supports the `--help` option for detailed usage information.
A running [Bluetooth daemon (BlueZ)](http://www.bluez.org/) is required.

Installation
------------

First, install D-Bus and Bluetooth libraries on your system.
On Debian this can be achieved by running

    sudo apt install libdbus-1-dev libbluetooth-dev

Then, run the following command to install BLEZ tools

    cargo install blez-tools

If you do not have Cargo on your system, you can use [rustup](https://rustup.rs/) for installing it.

