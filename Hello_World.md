# Deploying a Hello World App on the Internet Computer

This guide will walk you through the process of deploying a simple 'Hello World' application using the Internet Computer platform.

## Prerequisites
Before you begin, make sure you have the Internet Computer Software Development Kit (SDK) installed on your system. You can find the installation guide for your operating system below:
- [Install IC SDK for Linux](IC_SDK_Linux.md)
- [Install IC SDK for MacOS](IC_SDK_MacOS.md)
- [Install IC SDK for Windows](IC_SDK_Windows.md)

## Setting Up Your Identity
Your identity is required to interact with the Internet Computer network.
1. Create a new identity by following the instructions provided [here](DFX_Wallet.md).
2. Activate your new identity with this command:
   ```shell
   dfx identity use <identity_name>
   ```

## Creating a New Hello World Project
Start by generating a new project. This will create a basic 'Hello World' application:
```shell
dfx new hello
```

## Deploying Locally
Follow these steps to deploy your app on a local server:
1. Change to the project directory:
   ```shell
   cd hello
   ```
2. Start the local canister execution environment :
   ```shell
   dfx start --background
   ```
3. Deploy your application:
   ```shell
   dfx deploy
   npm start
   ```

### Accessing Your Local App
To view your app, open a web browser and navigate to:
```
http://localhost:8080
```

\## Deploying to the Internet Computer Mainnet
For deployment on the Internet Computer's main network:
1. Ensure you have a funded cycles wallet, as detailed [here](DFX_Wallet.md).
2. Deploy your project using this command:
   ```shell
   dfx deploy --network ic
   ```
