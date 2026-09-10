# Auto Synchronize forked repositories

This repository automates the synchronization of forked repositories for the GitHub namespace `VHDL`. The algorithm
lives in the reusable action [pyTooling/SynchronizeForks](https://github.com/pyTooling/SynchronizeForks); this
repository contributes only the
[workflow](https://github.com/VHDL/Synchronize/blob/main/.github/workflows/Synchronize.yml) calling it and the
configuration files (`*.repos`) listing the forks.


## Synchronized repositories

* OSVVM
  * `OSVVM` ⇐ [OSVVM/OSVVM](https://github.com/OSVVM/OSVVM) — `main`, `dev`
  * `OSVVM-Libraries` ⇐ [OSVVM/OsvvmLibraries](https://github.com/OSVVM/OsvvmLibraries) — `main`, `dev` *(disabled)*
  * `OSVVM-Scripts` ⇐ [OSVVM/OSVVM-Scripts](https://github.com/OSVVM/OSVVM-Scripts) — `main`, `dev`
  * `OSVVM-Common` ⇐ [OSVVM/OSVVM-Common](https://github.com/OSVVM/OSVVM-Common) — `main`, `dev`
  * `OSVVM-AXI4` ⇐ [OSVVM/AXI4](https://github.com/OSVVM/AXI4) — `main`, `dev`
  * `OSVVM-UART` ⇐ [OSVVM/UART](https://github.com/OSVVM/UART) — `main`, `dev`
  * `OSVVM-DPRAM` ⇐ [OSVVM/DpRam](https://github.com/OSVVM/DpRam) — `main`, `dev` *(disabled)*
  * `OSVVM-CoSim` ⇐ [OSVVM/CoSim](https://github.com/OSVVM/CoSim) — `main`, `dev` *(disabled)*
  * `OSVVM-Ethernet` ⇐ [OSVVM/Ethernet](https://github.com/OSVVM/Ethernet) — `main`
  * `OSVVM-Wishbone` ⇐ [OSVVM/Wishbone](https://github.com/OSVVM/Wishbone) — `main` *(disabled)*
  * `OSVVM-SPI` ⇐ [OSVVM/SPI_GuyEschemann](https://github.com/OSVVM/SPI_GuyEschemann) — `main` *(disabled)*
  * `OSVVM-VideoBus` ⇐ [OSVVM/VideoBus_LouisAdriaens](https://github.com/OSVVM/VideoBus_LouisAdriaens) — `master` *(disabled)*
  * `OSVVM-Documentation` ⇐ [OSVVM/Documentation](https://github.com/OSVVM/Documentation) — `main` *(disabled)*
* *others*
  * *(none configured)*


## Configuration File Formats

`.ALL.repos` lists the upstream organisations, one per line. Each of them has a matching `<organisation>.repos` file
listing its forks as `<upstream>=<fork>:<branches>`. A line starting with `#` is a comment. See the
[action's README](https://github.com/pyTooling/SynchronizeForks#configuration-file-formats) for the authoritative
description.


## GitHub CLI Documentation

See https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork
