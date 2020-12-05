## Proposal Name: `arGQL`

[![Version](https://img.shields.io/npm/v/ar-gql?style=flat&colorA=000000&colorB=000000)](https://www.npmjs.com/package/ar-gql)

## Summary:

A JavaScript/TypeScript package that makes interaction with the Arweave GraphQL endpoint simple and easy.

## Motivation:

With the launch of the [Arweave GQL Endpoint](https://arweave.net/graphql), there doesn't exist a simple way to interact with it in a JS/TS project.

I myself have implemented functions, but it would be extremely nice to have a generic function I can just import.

Also, querying for infinite responses and pagination isn't straight forward, this library would take care of that.

## Specification:

- `run()` - Query the Arweave GQL endpoint.
  - Takes in a GQL query and optional variables.
- `all()` - Retrieve **all** results for a specific GQL query.
  - Parses all pages returned.
- `tx()` - Retrieve all information about a specific Arweave transaction.
  - Significantly faster than `arweave.transactions.get()`
- `fetchTxTag()` - Retrieve the value of a specific Arweave transaction tag (if it exists).

## Team:

John Letey ([@johnletey](https://github.com/johnletey)):

- CTO @ [th8ta](https://th8ta.org).
- Co-Founder of [Verto](https://verto.exchange).
- Development Lead & Co-Founder [ArVerify](https://github.com/ArVerify).

## Timeline:

~ 1 to 2 weeks

## Grant Requested (DAI):

200 DAI (currently ~150 GBP)

## Ethereum Address:

`0x0f3F9D76D105E4F75171B3BA7f54094A4B2cc156`
