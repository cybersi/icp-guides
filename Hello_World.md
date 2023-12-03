# Hello World
Deploying Hello World

Switch to new identity you created [here](DFX_Wallet.md).

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

Create and top up cycles wallet as described [here](DFX_Wallet.md).

Deploy your project to the IC network:

```shell
dfx deploy --network ic
```
