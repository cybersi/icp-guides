## Deploying Hello World

### Create New Identity

Create a new identity and select it:

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

### Send ICP to Your DFX Account

Retrieve your account identifier:

```shell
dfx ledger account-id
```

### Check Balance

Check your ICP token balance on the network:

```shell
dfx ledger --network ic balance
```

### Quick Deployment

For a quick deployment:

```shell
dfx quickstart
```

### Manual Deployment Process

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
