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

## Example Output

```
--- System Info ---
     Static hostname: box
           Icon name: computer-desktop
             Chassis: desktop 🖥️
    Operating System: Fedora Linux 40 (KDE Plasma)    
         CPE OS Name: cpe:/o:fedoraproject:fedora:40
      OS Support End: Tue 2025-05-13
OS Support Remaining: 11month 2w 1d
              Kernel: Linux 6.8.10-300.fc40.x86_64
        Architecture: x86-64
     Hardware Vendor: ASUS
      Hardware Model: TUF GAMING B650-PLUS
    Firmware Version: 1654
       Firmware Date: Fri 2023-08-25
        Firmware Age: 9month 2d

--- non-default RPM packages ---
Name                                    Packager                                                         Version         License
polychromatic                           (none)                                                           0.8.3           GPL-3.0
amdgpu-install                          (none)                                                           6.0.60002       MIT
ffmpeg                                  RPM Fusion                                                       6.1.1           GPLv3+
HandBrake-gui                           RPM Fusion                                                       1.6.1           GPLv2+
steam                                   RPM Fusion                                                       1.0.0.79        Steam License Agreement and MIT
code                                    Visual Studio Code Team <vscode-linux@microsoft.com>             1.89.1          Multiple, see https://code.visualstudio.com/license
docker-ce-cli                           Docker <support@docker.com>                                      26.1.3          ASL 2.0
docker-ce-rootless-extras               Docker <support@docker.com>                                      26.1.3          ASL 2.0
docker-ce                               Docker <support@docker.com>                                      26.1.3          ASL 2.0
lazygit                                 (none)                                                           0.42.0          MIT
google-chrome-beta                      Chrome Linux Team <chromium-dev@chromium.org>                    126.0.6478.17   Multiple, see https://chrome.google.com/
containerd.io                           (none)                                                           1.6.32          ASL 2.0

--- snap ---
Name               Version          Rev    Tracking       Publisher   Notes
bare               1.0              5      latest/stable  canonical✓  base
core22             20240408         1380   latest/stable  canonical✓  base
gtk-common-themes  0.1-81-g442e511  1535   latest/stable  canonical✓  -
snapd              2.63             21759  latest/stable  canonical✓  snapd

--- flatpak ---
Name                            Application ID                         Version         Branch        Origin         Installation
Synology Assistant              com.synology.SynologyAssistant         7.0.2           stable        flathub        system
Heliguy                         io.github.flattool.Warehouse           1.6.2           stable        flathub        system
Small Mammal Collective         org.gnome.World.PikaBackup             0.7.2           stable        flathub        system
SpeedCrunch                     org.speedcrunch.SpeedCrunch                            stable        fedora         system
VideoLAN et al.                 org.videolan.VLC                       3.0.20          stable        flathub        system

--- cargo ---
agg v1.4.3 (/home/martinus/git/github.com/asciinema/agg):
    agg
cargo-update v13.4.0:
    cargo-install-update
    cargo-install-update-config
eza v0.18.16:
    eza
hexler v0.1.0 (/home/martinus/git/github.com/martinus/hexler):
    hexler
t-rec v0.7.6:
    t-rec
topgrade v14.0.1:
    topgrade
xd v0.0.4:
    xd

--- docker ---
REPOSITORY                             TAG       IMAGE ID       CREATED        SIZE
ghcr.io/open-webui/open-webui          main      adb86c02cf4b   2 weeks ago    3.39GB
ubuntu                                 22.04     52882761a72a   4 weeks ago    77.9MB
containrrr/watchtower                  latest    e7dd50d07b86   6 months ago   14.7MB
mcr.microsoft.com/devcontainers/base   jammy     10720142a5ba   6 months ago   666MB

--- AppImages ---
/home/martinus/Downloads/LM_Studio-0.2.12-beta.AppImage

--- /opt ---
/opt
├── brother
│   └── Printers
├── containerd  [error opening dir]
├── google
│   └── chrome-beta
└── omnitrace
    ├── bin
    ├── include
    ├── lib
    └── share

11 directories, 0 files

--- binaries not in RPM (slow, this can take a while) ---
/usr/local/bin
	ollama
	oversteer
/usr/bin
	brprintconflsr3_HLL2350DW
/usr/local/sbin
/usr/sbin
	lpc
/home/martinus/.local/bin
	chezmoi
	cpu-frequency
	cursor_hide
	cursor_show
	gra
	hugger
	hugger.sh
	in
	lock-kde.sh
	m
	ni
	pip
	pip3
	pip3.12
	setup_install_everything
	tacho
	test.sh
	unixtime

Generated 2024-05-27 18:34:19.268363 with https://github.com/martinus/swlist 1.1.0
```