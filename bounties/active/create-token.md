# Create Token Commands

**Bounty**: $300 USD paid in PSF tokens

## Overview

The [psf-bch-wallet](https://github.com/Permissionless-Software-Foundation/psf-bch-wallet) needs commands for creating and minting SLP token, including NFTs and Group tokens.

## Scope
The scope of this task is to add five commands to psf-bch-wallet:
- **token-create-fungible** - Creates a new fungible SLP token class.
- **token-create-group** - Creates a new Group token class.
- **token-create-nft** - Creates a new NFT by consuming a Group token.
- **token-mint** - Mint new fungible or Group tokens.
- **send-baton** - Send a minting baton to a new address.

## Deliverables

Each of the five commands should be fully functional, in terms of creating and minting fungible, Group, and NFT tokens. The send-baton command should be able to send the mint baton to another address.

Beyond adding the basic functionality, the commands should include unit tests with 100% test coverage.
