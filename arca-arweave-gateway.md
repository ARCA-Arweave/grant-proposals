====Proposal name: ARCA-gateway====

====Summary====

An alternative Arweave gateway, the "ARCA Arweave Gateway" is based on MongoDB with extra web features. This supports ARCA goals in several ways such as -

* Help with decentralization by providing alternative clients to official Arweave team releases.
* Provide better performance to make the permaweb more usable and consumer friendly
* Speed up new node deploying by serving the blockweave faster to new nodes.
* Offer more features for developers such as rich ARQL queries.

This also lays the foundation for future ideas and grants as the software matures.  Perhaps this could be the start of the "Infuria.io" of Arweave.

====Motivation====

Arweave Gateways act as the front door to the Permaweb, in a sense that they serve content from the underlying blockweave over HTTPS.  Only a single full node client exists, developed by the Arweave team.  This client stores the entire block weave in a flat folder structure.  While this supports the mining use cases, it does not lend itself to high performing, scalable, cost effective, internet applications.  The current data storage can be improved for extra speed and less space requirements (approx 30-40%), which will bring down hosting costs. Additionally, starting new nodes becomes more and more challenging as data volume grows, this gateway will ease the process by providing other nodes a faster way to download the blockweave.

====Specification====

'''Stage 1 ''' COMPLETED

The first stage will set the ground work for the database and basic web layers for the new Arweave Gateway node.  It will leverage NodeJS and/or Python3.  MongoDB will be used as the database, which is well suited for Arweave's JSON files. At a high level, the gateway will pull block and transaction information from full Arweave nodes.  It will then optimize and serve this data for the broad usage of ARCA and the Arweave community.

* All existing blocks and transactions are going to be added in MongoDB
 * https://www.tutorialspoint.com/mongodb/mongodb_advantages.htm
* Data will have extra indexes like timestamps, block numbers, etc, for more flexibility and speed in queries
* An utility to append newly created blocks and txs to the DB will be included 
* Database will be integrated with a fast web server for retrieving tx and blocks by http(s)
* Node and gateway runners will be able to get weave data much easier in zipped chunks. This should help the torrent as well, because all previous data can be reused, and newer data can be added on top of existing.
* A GraphQL endpoint will be created for extra queries (right now arql is very limited)
  * Extra queries to include owner, target,fee, amount, time stamps, tx ids.  
* Testing will be performed by @Rehash with help from @vilenarios and ARCA when needed.  It is expected all delivered tools will work in a given production environment.
* All tools will be open sourced and step by step documentation to install the gateway, rebuild the DB and run the tools will be provided.
* Server specifications to be determined.

'''Stage 2'''

* Full Gateway features, like friendly transaction naming (similar to current gateway) and transaction uploading.
* Large transaction support
* GraphQL Schema support
* Solve compatiability issues with graphql with arweave-js
''Details TBA''

'''Stage 3'''

* Sharding and node integration. As the weave size gets larger it makes sense to have sharding supported by both gateways and nodes. 
''Details TBA''

====Team and previous work====

@rehash - Arweave Mining Pool

====Timeline====

3 weeks to develop and test all Stage 1 features.

ARCA can deploy the v2 of the software after it has been fully committed to the ARCA Community Apps github.

====Grant requested (DAI)====

1850 for Stage 1 + 500 for the GraphQL new queries that will be based on what new types ARCA/Arweave devs need, 2350 DAI Total for delivery of all Stage 1 features (COMPLETED)

1420 DAI For Stage 2 features

====Ethereum Address====

9c03e1ec536032bab21603e5f629f823a4bc6be0
