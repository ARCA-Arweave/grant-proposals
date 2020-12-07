## Proposal name: 
armob-2.0 - Phase 1

## Summary:
A mobile-friendly, offline-first, progressive web app providing full Arweave wallet functionality, transaction history, and ability to interact with Smartweave contracts, PSTs, and PSCs

## Motivation:
There is no existing web or mobile app that fills this need and users are forced to rely on block explorers to view wallet transaction history and command-line tools or the browser extension to upload content to Arweave.  Also, all the existing front-ends for popular Smartweave contracts charge fees and this will provide an alternative, minimally viable way to interact with Smartweave contracts

## Specification:
Extend the current [Armob 2.0 app](https://github.com/acolytec3/armob-2.0) with the following features:
- Support data transactions in various forms (file upload, take picture with device camera and post to Arweave, etc)
- Support custom tags on any/all transactions
- Expand transaction history to include filtering/searching on tags, etc
- Expanded PST interactions
    - View vaulted balances
    - Integrate Verto buy/sell functionality
- Additional support for Smartweave contract interactions
    - Interact with all exposed Smartweave functions
    - Read and view contract state
- Integrate ArweaveID support into wallet for both main wallet and in transaction history view
- Support storing multiple wallets locally and switching between them


## Team and previous work:
Team - acolytec3
Previous work - 
- [ArMob 2.0](https://github.com/acolytec3/armob-2.0) - Minimum viable version 
- [ArweaveIDv2](https://github.com/ARCA-Arweave/arweave-id-v2)
- [Armob 1.0](https://github.com/acolytec3/ArMob)
- [arweave-mnemonic-keys](https://github.com/acolytec3/arweave-mnemonic-keys)
- [arweave-browser-extension](https://github.com/acolytec3/arweave-browser-extension)

## Timeline:
- data transactions/tags/transaction history - 1 week
- enhanced PST integration/Smartweave interactions - 1 week
- ArweaveID integration - as soon as v3 is ready (or else I'll proceed with v2)
- Multi-wallet support - 1 week

## Grant requested (DAI):
1500 DAI

## Ethereum Address:
0xBcAfdD642118e5536024675e776d32413728dd08