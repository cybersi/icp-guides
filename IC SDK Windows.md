# Setting Up WSL for Windows 10/11

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

## Accessing Linux Files from Windows

Access Linux files from Windows by entering `\\wsl$` in the File Explorer address bar.

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

Install the Internet Computer SDK for Debian and Ubuntu:

```shell
sh -ci "$(curl -fsSL https://smartcontracts.org/install.sh)"
```

Log out and then log back in to ensure the SDK is properly initialized.

## Development with DFINITY

### Create New Identity

Manually create a new identity and use it:

```shell
dfx identity new <name>
dfx identity use <name>
```

### Create a New Hello World Project

```shell
dfx new hello
```

### Deploy Locally

Navigate to the project directory and start the local server:

```shell
cd hello
dfx start --background
dfx deploy
npm start
```

### Access the Local App

Open your web browser and go to:

```
http://localhost:8080
```

# Deploy on the Internet Computer Mainnet

## Send ICP to Your DFX Account

Retrieve your account identifier:

```shell
dfx ledger account-id
```

## Check Balance

Check your ICP token balance on the network:

```shell
dfx ledger --network ic balance
```

## Quick Deployment

For a quick deployment:

```shell
dfx quickstart
```

## Manual Deployment Process

### Create Wallet Canister

Obtain your principal identifier:

```shell
dfx identity get-principal
```

Create a new canister on the network and deposit ICP tokens into it:

```shell
dfx ledger --network ic create-canister <PRINCIPAL_ID> --amount <ICP_TOKENS>
dfx identity --network ic deploy-wallet <WALLET_CANISTER_ID>
```

### Deploy on the Internet Computer Mainnet

Deploy your project to the IC network:

```shell
dfx deploy --network ic
```

## Top-Up Canisters

Add cycles to your canister as needed:

```shell
dfx wallet --network ic send <CANISTER_ID> <AMOUNT_CYCLES>
```
