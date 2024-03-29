# Topping-Up Canisters with Cycles

### Get the Canister ID

You'll need Canister ID to perform the canister operations. You can obtain Canister ID by:

1. **Deploying the Project**:  
   Deploy your project and get the canister ID with:  
   ```shell
   dfx deploy --network ic
   ```
   
2. **Querying an Existing Canister ID**:  
   If your canister is already deployed, retrieve its ID with:  
   ```shell
   dfx canister id --network ic <canister_name>
   ```
   
3. **Checking Local Files**:  
   Alternatively, find the canister ID in the `canister_ids.json` file in your project directory.

## Topping-Up Canisters with DFX and Cycles Wallet

To top up your canisters, use DFX in conjunction with the Cycles Wallet:

1. **Sending Cycles**:  
   Execute the command to transfer cycles:  
   ```shell
   dfx wallet --network ic send <canister_id> <amount_cycles>
   ```
   
2. **Specifying Amounts in DFX 0.15.2+**:  
   In DFX version 0.15.2 and above, you can denote cycle amounts in various units:
   - `k` for thousands (e.g., `500k`)
   - `m` for millions (e.g., `5m`)
   - `b` for billions (e.g., `50B`)
   - `t` for trillions (e.g., `0.3T`)

   Refer to the [DFX and Cycles Wallet guide](DFX_Wallet.md) for more details.

## Topping-Up Canisters via NNS

1. **Navigating to NNS**:  
   Go to [NNS Canister Management](https://nns.ic0.app/canisters/) and log in.

### Linking Canisters to NNS

1. **Linking Your Canisters**:  
   In the "My Canisters" section, click the "Link Canister" button and add your canisters.
   
2. **Obtaining NNS Principal**:  
   Note your NNS Principal ID for later use.

### Adding NNS Principal as a Canister Controller

1. **Adding NNS Principal**:  
   To allow NNS to manage your canister, run:  
   ```shell
   dfx canister update-settings --add-controller <principal> <canister_id> 
   ```
   
   After this, you can view and manage your canister's cycles balance directly from NNS.
