# Installation of IC SDK on Linux (Debian, Ubuntu...)

## Updating System and Installing Dependencies

```shell
sudo apt update
sudo apt upgrade -y
sudo apt install curl libunwind-dev -y
```

## Installing Node.js (v21)

```shell
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
sudo apt install -y nodejs
```

## Installing IC SDK

Install the Internet Computer SDK:

```shell
sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)"
```

Log out and then log back in to ensure the SDK is properly initialized.

Check the DFX version:
```shell
dfx --version
```
