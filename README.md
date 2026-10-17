# Blackgold Mining Protocol

A modular, high‑performance mining system for Solana — derived from the open‑source ORE protocol (MIT License)

# Introduction

Blackgold is a next‑generation decentralized mining protocol built for the Solana blockchain.
It is derived from the open‑source ORE protocol (MIT License) and redesigned with a modern, modular architecture that supports:

deterministic entropy generation

secure commit–reveal mining rounds

flexible reward distribution

optional staking multipliers

developer‑friendly APIs and SDKs

Blackgold is engineered for reliability, extensibility, and long‑term sustainability.

# Architecture Overview
BlackGold is organized as a multi‑crate Cargo workspace, allowing each subsystem to evolve independently while remaining part of a unified protocol.

blackgold/
│
├── entropy-types/             # Shared structs (Var, Open, Reveal, etc.)
├── blackgold-entropy-api/     # Entropy instruction builders + PDA helpers
├── blackgold-entropy-program/ # On-chain entropy logic
│
├── blackgold-mining-api/      # Mining instruction builders + client SDK
├── blackgold-mining-program/  # On-chain mining logic
│
├── blackgold-stake-api/       # Staking instruction builders + client SDK
├── blackgold-stake-program/   # On-chain staking logic
│
└── README.md


Each crate is independently publishable on crates.io and designed for production‑grade use.

Key Components

# Entropy Engine

A secure commit–sample–reveal entropy protocol built around:

round‑ID based PDA structure

deterministic value generation

minimal compute footprint

single‑round sampling (optimized for Blackgold)

# Mining Protocol

Implements the full mining lifecycle:

round initialization

commit validation

entropy sampling

reveal verification

reward distribution

miner authority enforcement

# Staking System

Optional staking module providing:

stake/unstake flows

reward multipliers

miner eligibility logic

treasury‑controlled minting

# Developer SDKs
Rust‑based client APIs for:

mining

staking

entropy

PDA helpers

serialization utilities

# Relationship to ORE
Blackgold is not a GitHub fork of ORE, but it is derived from the open‑source ORE protocol, which is licensed under the MIT License.

## This allows:

### downloading the ORE source code

### modifying and extending it

### publishing new crates

### restructuring the architecture

### branding the protocol independently

Blackgold maintains attribution through this README and the included MIT license.

We acknowledge and appreciate the foundational work of Regolith Labs in creating ORE.

# License
Blackgold is released under the MIT License, identical to the license used by ORE.

This project includes modified components originally based on the open-source
ORE protocol (MIT License). Blackgold is an independent protocol with its own
architecture, extensions, and roadmap.

# Status
Active Development  
Blackgold is currently under construction. APIs, program logic, and documentation will evolve as the protocol matures.

# Roadmap
### Phase 1 — Core Infrastructure
- [ ] Publish `entropy-types` crate
- [ ] Publish `blackgold-entropy-api`
- [ ] Deploy `blackgold-entropy-program` to devnet

### Phase 2 — Mining Protocol
- [ ] Implement mining round lifecycle
- [ ] Integrate miner commit → sample → reveal flow
- [ ] Implement reward distribution logic
- [ ] Publish `blackgold-mining-api`
- [ ] Deploy `blackgold-mining-program` to devnet

### Phase 3 — Staking System
- [ ] Implement staking/unstaking flows
- [ ] Add reward multipliers
- [ ] Publish `blackgold-stake-api`
- [ ] Deploy `blackgold-stake-program` to devnet

### Phase 4 — Ecosystem Tools
- [ ] Miner CLI
- [ ] Indexer service
- [ ] Dashboard UI
- [ ] Testnet launch
- [ ] Mainnet launch

# Contributing
Contribution guidelines will be published once the initial architecture stabilizes.

# Contact
For inquiries, partnerships, or security reports:

Email: orionlumesystems@gmail.com
Website: https://blackgold.supply
