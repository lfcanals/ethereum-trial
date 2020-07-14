Tutorial here https://www.trufflesuite.com/tutorials/pet-shop

# How to run and play
Download Ganache (https://www.trufflesuite.com/ganache) to have an Ethereum
blockhain runner.


## How to run
Install Truffle with NPM:

  npm i -g truffle


# What I've done
The steps I followed:

# Init
Init project with Truffle:

  truffle init

# Define de Adoption contract
Create a new Adoption.sol file in contracts/ folder.
Contract is written in Solidity language.
It can be compiled with

  truffle compile

# Deploy the contract (migrate) into testing blockchain
With Ganache started up (since Truffle is ready to deploy in local blockchain
server), just migrate the contracts.

Previously, you need to create the `migrations/2_deply_contract.js´ 
code with the instructions to migrate Adoption contract.

Type

  truffle migrate

Check in Ganache the consumption of gas and the new created blockchains.


# Execute the tests
Be sure truffle-config.js has properly set the values for network:

  module.exports.networks.development = {
      host: "127.0.0.1",
      port: 7545,
      network_id: "*"
  }


and execute

  truffle test

