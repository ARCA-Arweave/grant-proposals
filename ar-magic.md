## Proposal Name: `arMagic`

## Summary:

A JavaScript/TypeScript package that makes interaction with the Arweave network painless and simple.

## Motivation:

With the launch of the [Arweave GQL Endpoint](https://arweave.net/graphql), there doesn't exist a simple way to interact with it in a JS/TS project.

I myself have implemented functions, and copy-n-paste them throughout my projects - but it would be extremely nice to have a generic function I can just import.

Also, querying for infinite responses and pagination isn't straight forward, this library would take care of that.

## Specification:

- `query()` - Function to query the Arweave GQL endpoint.
  - Takes in GQL query and optional variables.
- `all()` - Function to grab **all** results for a specific GQL query.
  - Parses all pages returned.
- `paginate()` - Function for infinate loading on sites.

Suggestion by [Ros](https://github.com/mcmonkeys1):
- `post()` - Function that posts an Arweave tx and automatically resends it if failed.

... plus any more functions that are needed ...

## Team:

John Letey ([@johnletey](https://github.com/johnletey)):

- Co-Founder of [Verto](https://verto.exchange).
- Development Lead @ [ArVerify](https://github.com/ArVerify).

## Timeline:

~ 1 to 2 weeks

## Grant Requested (DAI):

100 DAI

## Ethereum Address:

`0x0f3F9D76D105E4F75171B3BA7f54094A4B2cc156`
