# apt.mrawlik.com

APT repository for [Michał Rawlik](https://github.com/mrawlik)'s projects, for
Debian 12 (Bookworm), Ubuntu 24.04 and newer, on amd64.

## Setup

```sh
sudo curl -fsSLo /etc/apt/keyrings/mrawlik.gpg https://apt.mrawlik.com/mrawlik.gpg
printf 'Types: deb\nURIs: https://apt.mrawlik.com\nSuites: stable\nComponents: main\nSigned-By: /etc/apt/keyrings/mrawlik.gpg\n' \
  | sudo tee /etc/apt/sources.list.d/mrawlik.sources
sudo apt update
```

You can then use apt to install packages, for example `sudo apt install signum`. To update them, run `apt upgrade`.

To check the key, run `gpg --show-keys /etc/apt/keyrings/mrawlik.gpg`. It should
print this fingerprint:

```
2F6E 717B F5EA 6699 9222  53E2 EDEF 86CE 783B 2A0F
```

## Packages

[signum](https://github.com/mrawlik/signum) - Stamp a signature on PDFs

Every project in [`projects.txt`](projects.txt). Each package is built and
released in its own repository. This one only collects the latest release of each.

## Removal

```sh
sudo rm /etc/apt/sources.list.d/mrawlik.sources /etc/apt/keyrings/mrawlik.gpg
```

## Contact

dev@mrawlik.com
