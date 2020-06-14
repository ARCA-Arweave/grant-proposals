## Proposal name: ArweaveID V2
Author: acolytec3, Ros

## Motivation: 
ArweaveID V1 is a great concept for providing a standard way to manage a identity on Arweave but has several shortcomings, 
including lack of avatar support, misleading "Unix Time" field that can easily be spoofed, and no standardized library for creating/updating 
ArweaveID fields.

What is needed is a standardized, efficient way of creating and Updating ArweaveID records that also ensures that name uniqueness is preserved
and attempted name-stealing disregarded.

## Specification: 
ArweaveID V2 (hereafter V2) will revise the current transaction spec to include all ID fields (name, email, ethereum address, twitter
and discord) in transaction tags rather than transaction data to allow for efficient retrieval via GraphQL interface as well as abstract id lookup/posting 
and add support for a new avatar field.

## Deliverables:
1) A revised ArweaveID transaction spec as structured below, supported by a Typescript library that provides the three methods specified. 
2) An updated V2 permaweb app that allows users to easily check to see if an ArweaveID is available, create and update their ArweaveID,
and transparently migrates existing users from V1 to V2.

### Arweave-id Version 2 Transaction Structure
Tags
App-Name: "arweave-id"
App-Version: “X.X.0” <= TBD as per https://semver.org/ 
Type: "all" (this is a new type) <= may be dropped
UnixTime: "DONOTUSE" <= may be dropped
Name: supplied
Email: supplied
Ethereum: supplied
Twitter: supplied
Discord: supplied
Content-Type: supplied, if said media-type is supplied in transaction data
Data
The avatar picture file


### ArweaveID-V2 API

ArweaveIdInterface:
{
Name: string
emai?l: string
ethereum?: string
twitter?: string
discord?: string
avatarDataUri?: string
}

`getArweaveIdFromAddress(walletAddress: string, arweaveInstance: arweave): ArweaveIdInterface | string`
returns current ArweaveID details as an ArweaveIdInterface object of key/value pairs. 

`setArweaveIdData(data: ArweaveIdInterface, jwk: JwkInterface, arweaveInstance: arweave): string`
writes a single Arweave-id version 2 transaction to supersede all previous transactions and fills any missing data from previous transactions. 

`getAddressfromArweaveID(arIdName: string, arweaveInstance: arweave): string `
returns the wallet address with a valid claim to the name (based on earliest transaction by block time for an address that hasn't afterwards switched addresses)

## Team
acolytec3, rosmcmahon
https://github.com/ARCA-Arweave/arweave-id-v2

## Timeline
- Complete library implementation - 5 hours
- Build permaweb app - 10 hours

## Funding Request
 - 400 DAI 