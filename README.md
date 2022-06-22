# rust-counter-tutorial

## Smart Contract built for the NEAR Protocol using Rust that allows users to keep track of a count on chain.

## Features 
- Get the current count.
- Increment the count.
- Decrement the count.
- Reset the count.

## Interacting with the contract
  1. Make sure Rust, NEAR CLI and your NEAR Test Wallet have been configured.
      - Visit https://docs.near.org/docs/develop/basics/getting-started for more info.
  2. Clone this repository and navigate to the root folder within your terminal
  3. Compile the contract:
      cargo build --target wasm32-unknown-unknown --release
  4. Deploy the contract
      - Login to your near wallet by using the following command
          near login
      - Finalize contract deployment
          near deploy --wasmFile target/wasm32-unknown-unknown/release/rust_counter_tutorial.wasm --accountId YOUR_ACCOUNT_HERE
  5. Verify that you receive a success message similar to the one below:
      
      Scheduling a call: YOUR_ACCOUNT.testnet.increment()
      Receipt: 3r9VBxypkdMVJNzbmfUd1GYz4iHjdDM7VZX7DijZ9jg3
          Log [YOUR_ACCOUNT.testnet]: Increased number to 1
          Log [YOUR_ACCOUNT.testnet]: Make sure you don't overflow, my friend.
      Transaction Id 4Cc8BAj3NiMB2Z5XBPmozKJy2dGtpJSoSaA1m7hHxRGQ
      
   6. Once your transaction is successful you can interact with the contract by running:
        
        near call YOUR_ACCOUNT_HERE COMMAND --accountId YOUR_ACCOUNT_HERE
        
        - Available commands are:
           - get_num
           - increment
           - decrement
           - reset

## Languages, Frameworks and Concepts Used
- Rust
- Near Protocol
- Near CLI
- Near TestNet
- Borsh Serialization
