# Flipper Contract
Simple substrate smart contract
## Prerequisites
* Update your Rust environment
```
# Update your Rust environment by running the following command:
$ rustup component add rust-src --toolchain nightly

# Verify that you have the WebAssembly target installed by running the following command:
$ rustup target add wasm32-unknown-unknown --toolchain nightly
```
* Install the Substrate contracts node
```
$ cargo install contracts-node --git https://github.com/paritytech/substrate-contracts-node.git --tag <latest-tag> --force --locked
```
* Install the WebAssemvly binary
```
# For example, on Ubuntu or Debian, run the following command:
$ sudo apt install binaryen
```
* Install the cargo-contract package
```
# Install dylint-link, required to lint ink! contracts, warning you about things like using API's in a way that could lead to security issues:
$ cargo install dylint-link

# Install cargo-contract by running the following command:
$ cargo install cargo-contract --force

# Verify the installation and explore the commands avilable by running the following command:
$ cargo contract --help
```
## Build the contract
* Compile the flipper smart contract vy running the following command:
```
$ cargo +nightly contract build
```
## Run a Substrate smart contracts node
* Start the contracts node in local development mode by running the following command:
```
$ substrate-contracts-node --dev
```
* To interact with the blockchain, you need to connect to this node. You can connect to the node through a browser by opening the [Contracts UI](https://paritytech.github.io/contracts-ui/).
