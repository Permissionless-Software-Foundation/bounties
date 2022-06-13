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
- Update wallet to use Web 2 infrastructure

## Deliverables

Each of the five commands should be fully functional, in terms of creating and minting fungible, Group, and NFT tokens. The send-baton command should be able to send the mint baton to another address.

Beyond adding the basic functionality, the commands should include unit tests with 100% test coverage.

An additional item added to this bounty: Commands that instantiate minimal-slp-wallet need to be updated so that they can be configured to use web 2 OR web 3 infrastructure. Example:
- [These lines](https://github.com/Permissionless-Software-Foundation/psf-bch-wallet/blob/870782e9629ba30df379c6b3936ca137c474f2f9/src/commands/wallet-balances.js#L74-L79) need to be updated to look more like this:

```javascript
      // Configure the minimal-slp-wallet library.
      let advancedConfig = {
        interface: 'consumer-api',
        restURL: restServer
      }

      const useWeb3 = this.conf.get('web3')
      if(!useWeb3) {
        interface: 'rest-api',
        restURL: restServer
      }
```

That requires a new `web3` conf setting which should default to `true`. When set to `false` it will use the bch-api web2 infrastructure.
