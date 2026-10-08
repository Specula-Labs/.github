<div align="center">

# Specula Labs

**Watching the Stellar network so a bad account is visible before it is expensive.**

[![Network](https://img.shields.io/badge/network-Stellar-F59E0B?style=for-the-badge&logo=stellar&logoColor=white)](https://stellar.org)
[![Contracts](https://img.shields.io/badge/contracts-Soroban-111827?style=for-the-badge&logo=rust&logoColor=white)](https://soroban.stellar.org)
[![License](https://img.shields.io/badge/license-MIT-6B7280?style=flat&logo=opensourceinitiative&logoColor=white)](#repositories)

</div>

## What Specula Labs builds

Specula is a risk layer for the Stellar network. It screens Stellar account activity, publishes Soroban contract flags, and reports network health, so builders and analysts can look at an account before they trust it.

## Two halves, one signal

| Component | What it does | Built with |
| --- | --- | --- |
| `specula-contracts` | Soroban contract holding authorized agents, a configurable score threshold, and the latest flag per subject | Rust, Soroban SDK |
| `specula-api` | Read-only service that scores Stellar accounts from Horizon and reads contract events from Stellar RPC | Python, FastAPI |
| `specula-app` | Dashboard for screening accounts and reviewing Soroban contract flag events | Next.js, TypeScript |

## Where Stellar comes in

Everything Specula does is anchored to Stellar. Screening reads account history from Horizon. Flags are written by a Soroban smart contract and published as on-chain events that any Stellar RPC client can read. The dashboard reports Stellar network status and Soroban RPC health, and links every account, contract, and transaction to the Stellar Expert explorer.

No part of the stack holds a signing key, and none of it submits a transaction. The whole surface is Stellar read paths plus one Soroban contract that authorized agents write to.

## Repositories

- [specula-contracts](https://github.com/Specula-Labs/specula-contracts) - the Soroban contract
- [specula-api](https://github.com/Specula-Labs/specula-api) - the screening and event service
- [specula-app](https://github.com/Specula-Labs/specula-app) - the dashboard

`Stellar` · `Soroban` · `Rust` · `Python` · `TypeScript`
