# Wallet Service

**Bounty**: 75 PSF per month

- _Up to 3 eligible bounties are available_

## Overview

The PSF community uses blockchain-services delivered over the IPFS network. While the PSF is blockchain agnostic and works with several blockchains, the primary blockchain used is Bitcoin Cash (BCH). As captured in [this video](https://youtu.be/45YEeZi_8Kc), the PSF community requires several redundant wallet service providers.

This bounty is currently eligible for community members who would like to host a copy of the BCH [Cash Stack](https://psfoundation.cash/blog/cash-stack), in order to provide wallet services for PSF software.

## Scope

The scope of the work is to set up and maintain a copy of the [Cash Stack](https://psfoundation.cash/blog/cash-stack) for the BCH blockchain. This requires running a Docker container for each of the following software packages:

- [ipfs-bch-wallet-service](https://github.com/Permissionless-Software-Foundation/ipfs-bch-wallet-service) IPFS-based back-end wallet service.
- [bch-api](https://github.com/Permissionless-Software-Foundation/bch-api) REST API server.
- [SLPDB](https://github.com/Permissionless-Software-Foundation/docker-slpdb) SLP Token indexer.
- [Fulcrum](https://github.com/Permissionless-Software-Foundation/docker-fulcrum) BCH indexer.
- [BCHN Full Node](https://github.com/Permissionless-Software-Foundation/docker-bchn)

A single desktop computer with 32GB of memory and a 1TB SSD drive is capable of running all the above software. Pre-synced databases can be downloaded over IPFS, from the [CashStrap page](https://fullstack.cash/cashstrap). These pre-synced databases make it much faster and easier to setup the above software.

Help and guidance with setting up the service correctly can obtained in [this Telegram channel](https://t.me/bch_js_toolkit). Before starting work on this bounty, ensure that it is still eligible by asking in the Telegram channel.

## Deliverables

An independent piece of software will collect hourly metrics on each wallet service and publish the results in the [P2WDB](https://github.com/Permissionless-Software-Foundation/ipfs-p2wdb-service). These metrics will be used to assess eligibility for the bounty.

In order to be eligible to collect this bounty, the following deliverables must be reviewed and accepted by the [Technical Steering Committee](https://github.com/Permissionless-Software-Foundation/TSC):

- The wallet service must be accessible over the internet via an IPFS Circuit Relay.
- The wallet service must achieve an uptime of 25 days within a month, based on collected metrics.
- The operator is required to update the software at least once per month, by pulling the latest code from GitHub.
