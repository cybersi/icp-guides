# DFX Identity and Cycles Wallet

## Create New Identity

To create a new identity in DFX, follow these steps:

1. **Create the identity** by running:
   ```shell
   dfx identity new <name>
   ```

2. **Select the created identity** for use:
   ```shell
   dfx identity use <name>
   ```

## Send ICP to DFX Account and Check the Balance

1. **Retrieve your account identifier** with:
   ```shell
   dfx ledger account-id
   ```

2. **Check your ICP token balance** by executing:
   ```shell
   dfx ledger --network ic balance
   ```

## Create Cycles Wallet

### Quick Method

For a quick setup of your identity and/or wallet:

- **Run the quickstart command**:
  ```shell
  dfx quickstart
  ```

### Manual Method

If you prefer manual setup:

1. **Create a new canister** and deposit ICP tokens into it:
   ```shell
   dfx identity get-principal
   dfx ledger --network ic create-canister <PRINCIPAL_ID> --amount <ICP_TOKENS>
   ```

2. **Deploy the wallet code**:
   ```shell
   dfx identity --network ic deploy-wallet <WALLET_CANISTER_ID>
   ```

3. **Check the cycles wallet balance**:
   ```shell
   dfx wallet --network ic balance
   ```

## Topping up Cycles Wallet

To add more funds to your cycles wallet:

1. **Obtain your wallet address**:
   ```shell
   dfx identity --network=ic get-wallet
   ```

2. **Top-up your cycles wallet** with the desired amount of ICP tokens:
   ```shell
   dfx ledger --network=ic top-up --amount <ICP_TOKENS> <WALLET_CANISTER_ID>
   ```
