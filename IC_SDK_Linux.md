# Installation of IC SDK on Linux (Debian, Ubuntu)

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
sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)"
```

Log out and then log back in to ensure the SDK is properly initialized.

## Accessing Linux Files from Windows

Access Linux files from Windows by entering `\\wsl$` in the File Explorer address bar.
