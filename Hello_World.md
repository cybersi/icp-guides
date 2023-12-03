# Deploying Hello World App

### Prerequisites
Install IC Software Development KIT (SKD):
- [Linux](IC_SDK_Linux.md)
- [MaxOS](IC_SDK_MacOS.md)
- [Windows](IC_SDK_Windows.md)

### Select the Identity
Create a new [identity](DFX_Wallet.md) and select it:

```shell
dfx identity use <name>
```

## Create a New Hello World Project

```shell
dfx new hello
```

## Deploy Locally

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

## Deploy on the Internet Computer Mainnet

Create cycles wallet and top-it-up as described [here](DFX_Wallet.md).

Deploy your project on the IC network:

```shell
dfx deploy --network ic
```
