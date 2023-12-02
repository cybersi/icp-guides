# Installation of IC SDK on Windows (WSL)

## Enabling Windows Subsystem for Linux

1. Go to **Control Panel** → **Programs** → **Turn Windows features on or off**.
2. Check the box for **Windows Subsystem for Linux**.
3. Click **OK** and reboot your system when prompted.

## Installing the Linux Subsystem

Open Command Prompt as Administrator and execute the following commands:

```shell
wsl --update
wsl --set-default-version 2
wsl --list --online
wsl --install -d Debian
```

# Linux Setup (Debian, Ubuntu)

## Updating System and Installing Dependencies

```shell
sudo apt update
sudo apt upgrade -y
sudo apt install curl libunwind-dev -y
```

## Installing Node.js (v21)

```shell
curl -SLO https://deb.nodesource.com/nsolid_setup_deb.sh
sudo chmod 500 nsolid_setup_deb.sh
sudo ./nsolid_setup_deb.sh 21
sudo apt install nodejs -y
```

## Installing IC SDK

Install the Internet Computer SDK:

```shell
sh -ci "$(curl -fsSL https://smartcontracts.org/install.sh)"
```

Log out and then log back in to ensure the SDK is properly initialized.

## Accessing Linux Files from Windows

Access Linux files from Windows by entering `\\wsl$` in the File Explorer address bar.
