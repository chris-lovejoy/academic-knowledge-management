# Decentralised storage of health data

### Metadata
topics: #decentralised-storage #blockchain #health-data #health-records 
type: #topic



### Self-test and recall questions
- what are the main protocols for decentralised storage of data? what are their differences?
- how does IPFS differ to current internet based storage?
- what are off-chain data protocols? what are some examples?


### Remaining to do / to understand
- what's the difference between the file storage protocols and off chain data protocols?
- Arweave enables 'permanent storage by "creating crypto-economic incentives for miners to replicate as much data as possible."' - how exactly does that work?

---

## Summary and high-level thoughts

In terms of maturity, my take is that the ecosystem of off-chain storage solutions is not yet where it needs to be to build out some of the more advanced use cases some developers might want. Some challenges here are real-time data, conflict detection and conflict resolution, write authorization, documentation, and general developer experience.


#### The evolution of decentralised storage
-   IPFS started it - but people have to pin the data. Persistence not guaranteed
-   Filecoin - basically you encourage other people to pin data on IPFS for you
-   estuary - filecoin but with better user experience
-   chainsafe, kiko + others - building the decentralised gold standard solutions


#### Contract-based vs permanent storage
Contract based examples: **Filecoin, Storj, Sia, SAFE**

Filecoin uses contract-based storage: Contract-based storage can be more simply thought of as a pay-as-you-go model. Users pay a network of nodes that store X bytes of data for Y period of time with Z retrievability guarantees. Storj, Sia and SAFE use the same model.

Permanent storage: arweave

With permanent storage, users pay a one-time, up-front fee to store the data _forever_. Permanent storage creates an entirely new market (we’ll get to this later). The Arweave protocol accomplishes this by leveraging crypto-economic game theory and creating an endowment to compensate miners for ensuring data availability, reliability and permanence.

Arweave introduces an entirely new economic model to the market, one that was never possible before the advent of permissionless crypto networks.


#### Cloud -> fog computing
Various organizations are now working towards transforming cloud computing into “Fog Computing”, a blockchain-based decentralized network of computing power that is globally scalable. Fog computing bridges the gap between the cloud and devices that produce data. It makes storage not only more secure but also more economical.



## Specific protocols and services 

### IPFS
Currently the Internet works off a location based addressing where you go to a URL like medium.com which has an IP of X.X.X.X and then you get served your articles.

Instead, what IPFS does is it serves information based on **_what it_** is as opposed to **_where it is_** (location). With their routing algorithms, you can choose where you get your content from and you can set your privacy of what peers/nodes you trust to receive your files which is quite interesting.

![[how IPFS works.png|500]]

### Storj
The storage side of Storj is decentralized. However, the settlement and indexing functions are centralized. Developers can test their storage capabilities on its alpha network.

It recently launched an evolved version of itself, called Tardigrade, an S3 compatible Ethereum cloud storage platform for developers using the Storj network. Storj compensates hosts in STORJ tokens for unused storage space and then makes it available for Tardigrade users.

CEO says focussing on storage for developers - therefore indirectly serving consumers (rather than consumers directly like e.g. DropBox)


### Swarm
https://www.ethswarm.org/

"for a sovereign digital society"

Based on the Ethereum cloud, Swarm is quite similar to Storj. It offers storage as well as communication services through a peer-to-peer network. Swarm incentivizes participants through BZZ tokens, enforced using smart contracts.

In June 2021 Swarm finally launched their system on the mainnet. This system had been under development for four years. Based on the Ethereum web3 stack, it offers various base layer services for web3 that support _decentralized storage_.


### Siacon by Sia
Sia is an early project that started back in 2013 at HackMIT and officially launched in 2015. It aims to leverage underutilized hard drive capacity around the world to create a data storage marketplace which is more efficient and cheaper to current solutions. They have a working product and have interesting design features.

The Siacoin platform places an emphasis on Proof-of-Work (PoW) and has its own ASIC chips for Siacoin mining. It also uses file contracts (like smart contracts) to determine storage requirements, as well as a strong Proof-of-Storage (PoS) algorithm to secure and validate file contracts on the network.


### MaidSafe
MaidSafe began in 2006 as a small team managing the Safe network. It offers a global network of storage nodes running Vault software. It is an open-source project in which anyone can easily become a storage provider, subject to resource testing. It also allows users to access all public information on the Safe network.

The Safe project offers an API for developers to directly interact with the network. Users pay in Safecoin to store data. Hosts, or farmers, receive Safecoin for storing data. Although developed, it is still a work-in-progress as new features get added at regular intervals.


### Burst
Burst, the company behind Burstcoin, originally made its name as the developer of the world’s first Proof-of-Capacity coin. It also developed the first blockchain to implement complete smart contracts. It is successfully working towards a cross-platform mobile wallet, called Phoenix. In the long term, Burst plans to launch its PoC3 protocol. It is first trying to tap all the unused hard-drive space and then use that space for storage.

In addition to the above-listed projects, various other groups are working towards different types of storage solutions. These include 0Chain, Archon Cloud, TrustSQL, Lambda, OneThing Cloud, TOP Network, and Internxt, to name a few.


### Arweave
Arweave is different to the other projects outlined here in that it enables permanent storage

This has many use cases, such as:
1.  Journalists who want to make sure their reporting is available forever to shine light on the truth;
2.  Political dissidents who want to ensure that governments can’t censor their thoughts;
3.  Lawyers working on personal estates or trusts;
4.  NGOs or foundations who want to store their records forever;
5.  People who want to store personal memories for distant future generations.

You have to pay a much higher cost up front cf. say AWS. 18x more expensive per GB right now.

Many DApps have shifted to it, like SushiSwap, UniwSwap, yearn.finance.

It ensures permanent storage by "creating crypto-economic incentives for miners to replicate as much data as possible."


## Off chain data protocols
https://edgeandnode.com/blog/defining-the-web3-stack

"In addition to file storage and on-chain storage, you may also need to store data off-chain. You might use these types of solutions similarly to how you might use a database in a traditional tech stack, but instead they are replicated across n number of nodes on a decentralized network, and therefore more reliable (at least in theory)."

A few options are:
-   [Ceramic Network](https://ceramic.network/) - a decentralized, open source platform for creating, hosting, and sharing data. Ceramic also has a nice identity protocol that I’ll talk about later. Probably my favorite off-chain storage solution at the moment. [Here’s](https://twitter.com/ceramicnetwork/status/1364631929262235648) a pretty nice demo.
-   Textile [ThreadDB](https://docs.textile.io/threads/) - a multi-party database built on IPFS and Libp2p. If I understand correctly, it may be going through a big API change at the moment. I’ve tried it and it shows some promise, but the docs and DX need some improvement.
-   [GunDB](https://gun.eco/) - a decentralized, peer-to-peer database. Gun has been around for quite sometime and [some pretty interesting applications](https://www.starlinglab.org/challenges/) have been built with it.


---

## References
- Papers:
	- [[Blockchain-Based Access Control Scheme for Secure Shared Personal Health Records over Decentralised Storage]]
	- [[A Scoping Review of Integrated Blockchain-Cloud (BcC) Architecture for Healthcare - Applications, Challenges and Solutions]]
	- [[A Secure Storage and Sharing Scheme of Stroke Electronic Medical Records Based on Consortium Blockchain]]
	- [[Authorized Shared Electronic Medical Record System with Proxy Re-Encryption and Blockchain Technology]]
	- [[Blockchain Personal Health Records - Systematic Review]]
	- [[Blockchain-Enabled iWellChain Framework Integration With the National Medical Referral System - Development and Usability Study]]
	- [[Cybersecurity, Data Privacy and Blockchain - A Review]]
	- (NOTE: links to other papers don't exist, as other paper summaries not uploaded in this demo vault)
- Articles:
	- Overview of storage protocols: https://pixelplex.io/blog/decentralized-storage/
	- The decentralised storage war - filecoin vs arweave - Coin market cap: https://coinmarketcap.com/alexandria/article/the-decentralized-storage-war-filecoin-vs-arweave
	- The web3 stack - Edge and Node: https://edgeandnode.com/blog/defining-the-web3-stack

