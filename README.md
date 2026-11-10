# CryptoCoin – Blockchain Cryptocurrency Simulation

## Overview

CryptoCoin (DSCoin) is a Java-based cryptocurrency simulation that explores the fundamental concepts of blockchain technology, secure transaction processing, mining, and transaction verification.

The project models a digital currency system where members can transfer coins, miners validate transactions and create new blocks, and cryptographic hashing helps maintain the integrity of transaction records.

It explores two blockchain environments: an honest blockchain and a malicious blockchain with competing branches.

## Key Features

- **Coin Management:** Models digital coins with unique identifiers and ownership records.
- **Transaction Processing:** Supports the lifecycle of coin transfers between members.
- **Transaction Queue:** Organizes pending transactions using a FIFO queue.
- **Blockchain Structure:** Links transaction blocks using cryptographic hashes.
- **Merkle Trees:** Summarizes transactions and supports efficient transaction inclusion proofs.
- **Proof-of-Work Mining:** Uses nonce-based hashing to satisfy block difficulty requirements.
- **Double-Spending Detection:** Defines validation rules to prevent the same coin from being spent more than once.
- **Honest and Malicious Blockchain Models:** Explores linear chains, competing branches, and valid-chain selection.

## Technology Stack

- **Programming Language:** Java
- **Cryptographic Hashing:** SHA-256-based hashing
- **Data Structures:** Linked lists, queues, arrays, and Merkle trees
- **Core Concepts:** Blockchain, proof of work, transaction validation, and cryptographic integrity

## System Architecture

The project is organized into the following components:

| Component | Responsibility |
|---|---|
| `Transaction` | Represents a transfer of a coin between members |
| `TransactionQueue` | Maintains pending transactions |
| `TransactionBlock` | Groups transactions into a block |
| `MerkleTree` | Generates transaction summaries and supports membership verification |
| `Members` | Represents participants and their coin-related operations |
| `Moderator` | Manages initial coin distribution |
| `BlockChain_Honest` | Models a linear blockchain with honest mining |
| `BlockChain_Malicious` | Models competing blockchain branches and valid-chain selection |
| `DSCoin_Honest` | Holds the main components of the honest cryptocurrency system |
| `DSCoin_Malicious` | Holds the components of the malicious blockchain model |

## Transaction Workflow

The intended transaction lifecycle follows these steps:

1. **Initialization:** A moderator distributes unique digital coins to members.
2. **Transaction Creation:** A member initiates a coin transfer to another member.
3. **Queue Management:** The transaction is added to the pending transaction queue.
4. **Validation:** A miner checks coin ownership and detects potential double spending.
5. **Block Creation:** Valid transactions are grouped into a transaction block.
6. **Merkle Tree Construction:** A Merkle root is calculated to summarize the block's transactions.
7. **Mining:** A nonce is calculated to produce a block digest satisfying the proof-of-work condition.
8. **Blockchain Insertion:** The mined block is linked to the existing blockchain.
9. **Transaction Verification:** A Merkle inclusion proof and block hashes can be used to verify a confirmed transaction.

## Blockchain Models

### Honest Blockchain

The honest blockchain assumes miners follow transaction validation rules. Valid blocks are appended sequentially to the existing blockchain.

### Malicious Blockchain

The malicious blockchain model considers situations where invalid blocks or competing branches may exist.

The system is designed to identify valid chains by checking transaction validity, Merkle tree consistency, and block digests. New blocks are attached to the longest valid chain.

## Security Concepts

The project explores several blockchain security mechanisms:

- **Cryptographic Integrity:** Hashes make modifications to recorded block data detectable.
- **Transaction Validation:** Ownership history is checked before approving transfers.
- **Double-Spending Prevention:** Previously spent coins are rejected during validation.
- **Proof of Work:** Mining requires computational effort to produce a valid block digest.
- **Merkle Proofs:** Transaction membership can be verified without processing every transaction in the block.

## Repository Structure

The Java source code is organized into classes for transaction management, blockchain operations, mining, member management, and cryptographic verification.

## Project Scope

CryptoCoin is an educational blockchain simulation designed to demonstrate cryptocurrency internals through data structures and algorithms.

It is not intended to operate as a production cryptocurrency network. The repository explores the architecture and algorithms of the system, and some implementation components may require further completion or testing.

## Future Improvements

- Complete and test the end-to-end transaction lifecycle.
- Add automated unit and integration tests.
- Implement digital signatures for transaction authentication.
- Introduce persistent storage for blockchain records.
- Add networking between independent blockchain nodes.
- Improve transaction validation and mining performance.
