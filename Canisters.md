# CANISTERS

## Topping-up Canisters

To get canister ids deploy the project with:

```shell
 dfx deploy --network ic
```
or request canister id with:

```shell
dfx canister id --network ic <canister_name>
```

or

open canister_ids.json

### Using DFX and Cycles Wallet

Topping-up canisters using [DFX and Cycles Wallet](DFX_Wallet.md):

```shell
dfx wallet --network ic send <canister_id> <amount_cycles>
```
In DFX 0.15.2+ you can define cycles amount also as:
- k for 000, e.g. 500k
- m for 000_000, e.g. 5m
- b for 000_000_000, e.g. 50B
- t for 000_000_000_000, e.g. 0.3T

## Using NNS
Navigate to: [https://nns.ic0.app](https://nns.ic0.app/canisters/) and log in.

### Link Canisters
Click Link Canister Button in the My Canisters section and add your canisters.


Copy your NNS Principal.

### Add NNS Principal as a Canister Controller

Add principal as a Canister Controller:

```shell
dfx canister controllers add <canister_id> <principal>
```

Now you can see the cycles balance and top-up the canisters directly from NNS
