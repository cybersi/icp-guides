
## DFX Identity and Cycles Wallet Creation

### Create New Identity

Create a new identity and select it:

```shell
dfx identity new <name>
dfx identity use <name>
```

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

## Quick Method

For a quick deployment:

```shell
dfx quickstart
```

## Manual Method

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

## Top-Up Canisters

Add cycles to your canister as needed:

```shell
dfx wallet --network ic send <CANISTER_ID> <AMOUNT_CYCLES>
```
