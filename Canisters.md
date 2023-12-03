#CANISTERS

##Topping-up Canisters

###Using DFX and Cycles Wallet


Topping-up canisters:

```shell
dfx wallet --network ic send <canister_id> <amunt in cycles>
```
Since DFX 0.15.2 you can define cycles amount also as:

k for 000, e.g. 500k
m for 000_000, e.g. 5m
b for 000_000_000, e.g. 50B
t for 000_000_000_000, e.g. 0.3T

Create a new identity:

```shell
dfx canister controllers add <canister_id> <principal>
```
