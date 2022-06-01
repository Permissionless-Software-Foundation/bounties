# Multi-signature Minting

**Bounty**: 4,000 PSF

## Overview

The PSF aspires to be a DAO, and in order to do that, we need to decentralized the ability to bring new PSF tokens into existence. This power should not be in the hands of one individual, but be controlled by a quorum of top community members.

## Scope

The slpjs JavaScript library has a [2-of-2 multisig SEND example](https://github.com/simpleledger/slpjs#send---send-tokens-from-2-of-2-multisig-p2sh). Minting tokens with a MINT command is similar to sending tokens with a SEND command, the primary difference being the content of the OP_RETURN. But the mechanics of constructing a multisig transaction are the same. This code example provides a great starting point for research.

In addition, it may be necessary to generate a partially signed transaction. The [collaborative transaction code examples](https://github.com/Permissionless-Software-Foundation/bch-js-examples/tree/master/applications/collaborate) contain code for generating such transactions with bch-js.

The slpjs code example needs the following changes to be usable by the PSF:

- It should use bch-js instead of slpjs or BITBOX.
- It should use bch-api and call api.fullstack.cash instead of rest.bitcoin.com.
- It should use 3-of-5 signatures instead of 2-of-2.
- The OP_RETURN and transaction output should follow the [MINT command](https://github.com/simpleledger/slp-specifications/blob/master/slp-token-type-1.md#mint---extended-minting-transaction) instead of the [SEND command](https://github.com/simpleledger/slp-specifications/blob/master/slp-token-type-1.md#send---spend-transaction).

## Deliverables

In order to eligible to collect this bounty, the following deliverables must be reviewed and accepted by the [Technical Steering Committee](https://github.com/Permissionless-Software-Foundation/TSC):

- A JavaScript example script that can generate 5 random key pairs. A key pair is is a WIF private key and a BCH public address.
- A JavaScript example script that can mint new tokens with 3-of-5 signatures.
- A JavaScript example script that can move the minting baton to a new address, with 3-of-5 signatures.
- (optional) An npm library containing transaction helper methods, used by the above scripts.

The above deliverables must meet the following requirements:

- Use P2SH (pay to script hash) addresses.
- Depends only on bch-js library, and does not depend on slpjs or BITBOX
- Can generate the multisig scriptsig required for multisignature transactions.

## Completion Information

This bounty was completed. Through the combined effort of PSF members trout, Stoyan, and Sam, we now have the ability to execute SLP minting operations from a multisignature wallet. This research is being developed into [psf-multisig-minting](https://github.com/Permissionless-Software-Foundation/psf-multisig-minting) wallet CLI app.
