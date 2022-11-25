---
layout: default
---

<a href="/">Back</a>

# Alembic App-Chain Scaling Solution

The first version of Alembic App-chain service consists in deployment and management  of an Optimism instance dedicated to your application (optimistic rollup Layer 2 that settles on Ethereum mainnet).

## App-Chain

An application-specific blockchain is exclusively designed to operate one specific application. This solution increases the performance of the app because there are no other apps to compete for computation or storage. Appchains give flexibility over the economic structure, governance structure, and consensus algorithm, and also allow for infrastructure related tokenomics.

## Optimistic rollup

An optimistic rollup is a scaling solution that involves moving computation and state storage off-chain. Optimistic rollups execute transactions outside of Ethereum, but post transaction data to Mainnet as calldata. Optimistic rollups are fully EVM compatible, thus any existing smart contract or wallet can be ported and used as is.

## Solution overview

App-chain
Consensus*


Agreement over the transactions and their ordering. Can enforce more complex rules to match the context of a consortium.
Settlement


Appending the state of the App-chain on the Ethereum mainnet, verifying cryptographic proofs and coordinating cross-chain asset transfers/arbitrary messaging.
Execution
EVM block by block computation from the pre-state to the new state, run transactions and transit to the post-state.

Ethereum Mainnet
Data Availability (DA)


Ensuring the transaction data of the rollup block headers has been published and made available allowing anyone can recreate the state.

*Consensus can be defined in accordance with the rules of your protocol

The tools (non-exhaustive list) deployed , tested and monitored (open source with MIT license)
op-batcher: L2-Batch Submitter, submits bundles of batches to L1
op-node: rollup consensus-layer client.
op-proposer: L2-Output Submitter, submits proposals to L1
Bridge for teleporting Token between L1 and L2 at low cost
block-explorer: Visualizing blocks, transactions, and blockchain network metrics

## Appchain Benefits

### Best in class User Experience

Transactions are included in the blockchain with the lowest latency possible
No need to preload an account with the native token
Gas fees can be entirely managed and paid by the network operator acting as a native relayer

### Cost effectiveness with high performance

Operation costs are predictable and independent of a third party token price
The appchain throughput is elastic and adapt to the activity volume
Publicly tested up to 2000 mint transactions-per-second (tps)

### Proven security and resilience

Optimistic rollups are securing ≈$3.5bn (TVL the 18th of Nov.)
Prevent third party manipulation of transaction block order and frontrun
The Rollup states are published as transaction data to Ethereum Mainnet, allowing anyone to execute the rollup’s transactions and rebuild its state if necessary. 
All the protocol data and certificates will be available on Ethereum Mainnet

### Future proof Long term support

This solution align your protocol infrastructure with the roadmap of Ethereum thus benefiting from all upcoming upgrades and tools (account abstraction, node client support)
Upgrade your protocol to the latest standard for blockchain applications

### Customizability

Guarantees the ability to adapt the service as the application grows in popularity and implement custom use cases ( KYC’d validators,  select which chains are able to bridge, …)
Ability to fork existing protocols and monetize them  (e.g. trading fees from an AMM or NFT marketplace).

### Value Capture

Strongly position application as a protocol with a own blockchain infrastructure with native Ethereum mainnet interoperability
Avoid spillover of marketing efforts, the cost of bringing a user on your app-chain only benefit the protocol stakeholders
More protocol token utility within the staking feature
