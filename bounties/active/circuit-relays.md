# Circuit Relays

**Bounty**: 15 PSF per month

## Overview

The PSF community uses blockchain-services delivered over the IPFS network. In order for users to consume these services, a robust network of [Circuit Relays](https://docs.libp2p.io/concepts/circuit-relay/) is required to help connect consumer nodes with service provider nodes across the mesh network. These Circuit Relays provide an essential networking component. They are not expensive to operate, but have specific requirements. This bounty will pay operators to setup and maintain Circuit Relays for the good of the PSF community.

The bounty is currently eligible for Circuit Relays set up in the following geographic locations. The operator does not need to be located in this region, but the server running the software must be located in these regions:

- South-East Asia, including Japan
- Australia
- South America
- Mainland China

## Scope

The scope of the work is to set up and maintain an [ipfs-service-provider](https://github.com/Permissionless-Software-Foundation/ipfs-service-provider) in Circuit Relay mode. An independent metrics service will monitor the uptime and availability of the software, and bounties will be rewarded each month if the software meets the required deliverables.

Help and guidance with setting up the service correctly can obtained in [this Telegram channel](https://t.me/bch_js_toolkit). Before starting work on this bounty, ensure that it is still eligible by asking in the Telegram channel.

## Deliverables

An independent piece of software will collect hourly metrics on each Ciruit Relay and publish the results in the [P2WDB](https://github.com/Permissionless-Software-Foundation/ipfs-p2wdb-service). These metrics will be used to assess eligibility for the bounty.

In order to be eligible to collect this bounty, the following deliverables must be reviewed and accepted by the [Technical Steering Committee](https://github.com/Permissionless-Software-Foundation/TSC):

- The Circuit Relay must have an ipv4 IP address accessible from the global internet. It must also have a domain name with an SSL certificate, to allow secure websocket connections. These two requirements will allow the software to achieve IPFS multiaddrs like this:
  - `/ip4/157.90.28.11/tcp/4001/p2p/QmedLCUDSSvsjfPt9rDm65drNL7Dzu1mk1JCRxu9yuxgLL`
  - `/dns4/ipfs-service-provider.fullstackcash.nl/tcp/443/wss/ipfs/QmedLCUDSSvsjfPt9rDm65drNL7Dzu1mk1JCRxu9yuxgLL`
- The Circuit Relay must achieve an uptime of 25 days within a month, based on collected metrics.
- The operator is required to update the software at least once per month, by pulling the latest code from GitHub.
