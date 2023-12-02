
## DFX Identity and Cycles Wallet Creation

### Create New Identity

Create a new identity and select it:

```shell
dfx identity new <name>
```

Select new identity:

```shell
dfx identity use <name>
```

Retrieve your account identifier:

```shell
dfx ledger account-id
```

### Send ICP to DFX account and Check the Balance

Check your ICP token balance:

```shell
dfx ledger --network ic balance
```

## Create Cycles Wallet

### Quick Method
Perform initial one time setup for your identity and/or wallet: 
```shell
dfx quickstart
```
### Manual Method

Create a new canister on the network, deposit ICP tokens into it and deploy wallet code:
```shell
dfx identity get-principal
dfx ledger --network ic create-canister <PRINCIPAL_ID> --amount <ICP_TOKENS>
dfx identity --network ic deploy-wallet <WALLET_CANISTER_ID>
```

## Top-Up Canisters

Add cycles to your canister as needed:

```shell
dfx wallet --network ic send <CANISTER_ID> <AMOUNT_CYCLES>
```
