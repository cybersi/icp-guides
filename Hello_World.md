# Deploying Hello World

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

Create and top up cycles wallet as described [here](DFX_Wallet.md).

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
