# Installation of IC SDK on Windows (WSL)

This guide provides steps for installing the Internet Computer Software Development Kit (IC SDK) on Windows using the Windows Subsystem for Linux (WSL).

## Enabling Windows Subsystem for Linux

Follow these steps to enable WSL on your Windows system:

1. Navigate to **Control Panel** → **Programs** → **Turn Windows features on or off**.
2. Select the checkbox for **Windows Subsystem for Linux**.
3. Click **OK** and reboot your system if requested.

## Installing the Linux Subsystem

Use the Command Prompt as an Administrator to install the Linux subsystem (Debian in this example):

```shell
wsl --update
wsl --set-default-version 2
wsl --list --online
wsl --install -d Debian
```

# Linux Setup (Debian, Ubuntu...)

After setting up WSL proceed with the following steps.

## Updating System and Installing Dependencies

Update your Linux system and install necessary dependencies:

```shell
sudo apt update
sudo apt upgrade -y
sudo apt install curl libunwind-dev -y
```

## Installing Node.js (v21)

Install Node.js version 21 using the following commands:

```shell
curl -SLO https://deb.nodesource.com/nsolid_setup_deb.sh
sudo chmod 500 nsolid_setup_deb.sh
sudo ./nsolid_setup_deb.sh 21
sudo apt install nodejs -y
```

## Installing IC SDK

To install the Internet Computer SDK:

```shell
sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)"
```
After installation, log out and log back in to ensure the SDK is properly initialized.

To check the DFX version:

```shell
dfx --version
```

## Accessing Linux Files from Windows

You can access your Linux files from Windows by typing `\\wsl$` in the File Explorer address bar.
