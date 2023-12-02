# Installation of IC SDK on MacOS

## Enabling Windows Subsystem for Linux

1. Go to **Control Panel** → **Programs** → **Turn Windows features on or off**.
2. Check the box for **Windows Subsystem for Linux**.
3. Click **OK** and reboot your system when prompted.

## Installing Homebrew (Package Manager)
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Installing Node.js
```shell
brew install node
```
## Installing IC SDK

Install the Internet Computer SDK:

```shell
sh -ci "$(curl -fsSL https://smartcontracts.org/install.sh)"
```
