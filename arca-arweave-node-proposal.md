# Proposal name: ARCA Arweave Node
### Authors : Vilenarios
## Summary: 
Host an official ARCA Arweave node and enable Gateway, IPFS Bridge and potentially mining to support internal and community initiatives. Specifically, a Gateway provides opportunities for ARCA development and further decentralizes the Arweave network by providing the second public Gateway service. 

## Motivation: 
There are several goals of hosting an Arweave node, benefiting ARCA and the broader Arweave community.  
1. Give the community another public Gateway to use other than arweave.net. 
2. Support internal ARCA development needs, like for PermaSnap or Mobile Wallet development. 
3. Give the community another public Mining endpoint to connect as a trusted peer. 
4. Potentially generate income for ARCA that could be used to offset server hosting charges or pay for other initiatives.


## Specification: 
The node specifications will be divided into separate components.
### Core Node
Setup a Ubuntu server running the latest version of Arweave.  Each ARCA member can request local admin privileges on the ARCA Arweave Node.  This will help them learn more about how the Arweave node software works.

It is recommended that this server has at least 4 cores, with 8GB of ram and 1TB of storage for the full Blockweave.  It also must have a public IP address with port forwarding on 443, with at least 50mbit network connection.

### Gateway
Configure and operate a public Arweave Gateway.  This will include a certificate for HTTPS and a public domain name eg.
https://permanent.to
https://arca.io
https://permaweb.com 
This Gateway can be used for internal ARCA development as well as public use.  As such, it is recommended to be isolated from other sensitive servers or data.
Gateway monitoring can be performed by Ubuntu monitoring tools like Graphite, with reports hosted on Grafana.
Document any steps involved in setting this up and host on the community Arweave wiki.

### IPFS Bridge
Configure an Arweave IPFS Bridge and document any standards with building applications that may leverage it.  
Document any steps involved in setting this up and host on the community Arweave wiki.

### Mining (Optional)
Enable RandomX hashing to support Arweave network security.  A centralized ARCA Arweave Wallet would have to be setup and managed for the small amount of Arweave that could be generated.  Ensure an optimal run state to maximize hash, while providing adequate performance to other server functions like Gateway.

Mining monitoring can be performed by Ubuntu monitoring tools like Graphite, with reports hosted on Grafana.
Please note that the main purpose of this server is to support an Arweave Gateway.  If it is determined (via monitoring and metrics) that Gateway performance is being impacted from mining, then max_miners should be reduced or potentially disable mining altogether. 

Mining may not be feasible with the first iteration of the ARCA Arweave Npde, as it will not have a lot of extra CPUs available.

### Future Plans
After the above components are deployed and operated successfully, some upgrades could be introduced into the ARCA Arweave node ecosystem, such as...

Better monitoring of Gateway related metrics and logs.
More Nodes to meet scale.
A decentralized wallet custody system for mining rewards.
Invest in mining pool software and running a community Arweave mining pool.

## Components:
The following milestones will be considered key deliverables.  When combined, they complete the first phase of ARCA Arweave Node.  Each milestone can have a corresponding cost and responsible party.  Larger milestones can be broken into individual sprints and goals.

Once the server is procured, It is expected that it will take approximately 2 weeks to have all milestones completed, pending any issues or roadblocks. 

### Core Node
Rent a cloud server for 3 months and deploy all software necessary to support Arweave.  Provide access to other ARCA members on request.

Responsible Party: @Garrett

### Gateway and IPFS Bridge
Configure Arweave IPFS Bridge and Gateway capabilities, including public DNS and certificates.  Document procedures and test connectivity

Responsible Party: @Vilenarios and @Garrett

### Mining (Optional)
Setup and Automate Arweave Mining including monitoring.  Establish central Arweave Wallet and custodian for block rewards.
Responsible Party: @Vilenarios
Wallet Custodian: @Vilenarios

## Team and previous work:
The following ARCA members will be responsible for this proposal and deliver the first capabilities for the ARCA Arweave Node.  Additionally, they will be responsible for operating the ARCA Arweave Node.

Gateway Configurations: @Vilenarios and @Garrett
Back End Node Operations: @Vilenarios

Ideally, ongoing ARCA Arweave Node operations will be a joint effort by ARCA members who are interested in node management.

## Risks:
The following are key risks that could adversely impact the project timeline and cost.

Unforeseen complexities with managing a gateway. 
Shared server access could lead to conflicting changes if change management isn't followed.
Centralized wallet control and misuse of funds.

## Timeline:
It is eastimated that setting up the ARCA Arweave Node, and all components, should take approximately 2 weeks.

## Marketing / Adoption:
Since this Arweave Node is not just meant to serve ARCA, but the broader community, an announcement should be made.  This announcement should include  (but wouldn’t be limited to) vision for ARCA Arweave Node, Gateway connectivity information and any other documentation.  It should be in a blog format, and can be published in common ARCA channels like Twitter and Arweave Discord.

## Budget:
### Core Node Hosting
$200 for dedicated server rental for 1 month = $600 for 3 months.

### Gateway and IPFS Bridge
$15 for domain registration for 1 year

Total for phase 1: $615 or 615 DAI

The first phase of ARCA Arweave Node will operate for 3 months, and determine the community benefits and whether or not it is worthwhile to continue hosting.  Other server hosting options can also be looked at as well to ensure ARCA gets the best resources at the most competitive price.

#### Funding Address: 0x26B751183814E6BA865c1B65BC00ab4d5501CE8C

