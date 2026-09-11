# Auto Synchronize forked repositories

This repository automates the synchronization of forked repositories for the GitHub namespace `VHDL`. The algorithm
lives in the reusable action [pyTooling/SynchronizeForks](https://github.com/pyTooling/SynchronizeForks); this
repository contributes only the
[workflow](https://github.com/VHDL/Synchronize/blob/main/.github/workflows/Synchronize.yml) calling it and the
configuration files (`*.repos`) listing the forks as well as the branches and tags to synchronize.


## Synchronized repositories

Which branches and tags of each fork are synchronized is in the `*.repos` files; repeating it here would only go out
of date.

* OSVVM
  * `OSVVM` ⇐ [OSVVM/OSVVM](https://github.com/OSVVM/OSVVM)
  * `OSVVM-Libraries` ⇐ [OSVVM/OsvvmLibraries](https://github.com/OSVVM/OsvvmLibraries) *(disabled)*
  * `OSVVM-Scripts` ⇐ [OSVVM/OSVVM-Scripts](https://github.com/OSVVM/OSVVM-Scripts)
  * `OSVVM-Common` ⇐ [OSVVM/OSVVM-Common](https://github.com/OSVVM/OSVVM-Common)
  * `OSVVM-AXI4` ⇐ [OSVVM/AXI4](https://github.com/OSVVM/AXI4)
  * `OSVVM-UART` ⇐ [OSVVM/UART](https://github.com/OSVVM/UART)
  * `OSVVM-DPRAM` ⇐ [OSVVM/DpRam](https://github.com/OSVVM/DpRam) *(disabled)*
  * `OSVVM-CoSim` ⇐ [OSVVM/CoSim](https://github.com/OSVVM/CoSim) *(disabled)*
  * `OSVVM-Ethernet` ⇐ [OSVVM/Ethernet](https://github.com/OSVVM/Ethernet)
  * `OSVVM-Wishbone` ⇐ [OSVVM/Wishbone](https://github.com/OSVVM/Wishbone) *(disabled)*
  * `OSVVM-SPI` ⇐ [OSVVM/SPI_GuyEschemann](https://github.com/OSVVM/SPI_GuyEschemann) *(disabled)*
  * `OSVVM-VideoBus` ⇐ [OSVVM/VideoBus_LouisAdriaens](https://github.com/OSVVM/VideoBus_LouisAdriaens) *(disabled)*
  * `OSVVM-Documentation` ⇐ [OSVVM/Documentation](https://github.com/OSVVM/Documentation) *(disabled)*
* *others*
  * *(none configured)*


## Configuration File Formats

`.ALL.repos` lists the upstream organisations, one per line. Each of them has a matching `<organisation>.repos` file
listing its forks as `<upstream>=<fork>:<branches>[:<tagPatterns>]`, the tag patterns being optional. A line
starting with `#` is a comment. See the
[action's README](https://github.com/pyTooling/SynchronizeForks#configuration-file-formats) for the authoritative
description.


## Documentation

See [pyTooling/SynchronizeForks](https://github.com/pyTooling/SynchronizeForks) for the action: its parameters, the
configuration file format, what it reports as an error, and how branches and tags are synchronized.
