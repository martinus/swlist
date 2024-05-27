# swlist - software lister

Produces a list of installed software that doesn't come from system's default packages.

## Installation

Just run

```sh
curl -fsSL https://raw.githubusercontent.com/martinus/swlist/main/swlist |python
```

## Supported Systems

* rpm
  * List all packages not installed from Fedora default packages
  * lists all binaries not comming from rpm packages
* snap
* flatpak
* cargo
* docker
* AppImages
* `/opt`
