# Protocol Specification
Please refer to the first document [0_Protocol.md](./0_Protocol.md) for a detailed explanation of the protocol. Data management requires a specific detail to track the evolution of "decentralised" data storage. Our definition of decentralised storage is one where identities who create data understand their power and are responsible for its maintainance. This entails that identities must choose what networks and the kind of data they decide to store based on the visions/goals of the network. A reference implementation of this decentralised network is currently built using reference of the ["Willow Protocol specs"](https://willowprotocol.org/specs/index.html#specifications) with a few modifications to the terms and their meanings. We add a consensus mechanism to the networks Culture store allowing network maintainers to come to consensus on what defines their culture and what doesn't. This is done by coding the Chiti, the soul identity or innate nature of a group. Defining the innate nature of the group is sometimes the toughest task of the network but can be achieved through a series of interactions and meetings with the initial network participants.

## User Interface
The user interface elements are generally encoded as a schema. This allows each application to attach their own "themes" to the UI elements allowing diversity in expression. A general schema may be implemented by the network for others to fork and modify.
* HTTP gateways - The end goal is to move identities onto a decentralised network. However, in order to reach out to the audience of today, interoperability with todays data is a must. The APIs built allow an individuals data/journal entries to be accessible via today modern browsers. This is generally done by creating RPCs to access the identities journal and a store maintaining the list of peer IDs along with their capabilities while accessing the store.
* Routing APIs - APIs identity nodes might have to implement (https://specs.ipfs.tech/routing/http-routing-v1/)

# Data formats

## Content Identifiers

Content Identifiers aim to address data using their content. This is generally done by hashing the data and using the hash as the ID. IPFS(InterPlanetary File System) went one step further and attached a multicodec table to allow different applications to "encode and decode" information basis an agreed upon protocol. This multicodec table is essentially a key value store with some metadata on what the meaning of the key is. CIDs are used by us to identify the root origin of an idea/goal. Maintaining a multicodec type table for ideas allows us to track the manifestation of an idea in the real world. By appending the corresponding idea ID to the message hash, one can achieve the following goals in a distributed systems network:
* Maintain a schema/language for the network to communicate. This schema is maintained through network governance where consensus is achieved on the meaning of the language and terms used. One can choose to "trust" a schema blindly. This is akin to the trust we place in the TCP/IP protocol to deliver our messages to the right destination.
* Blockchain consensus protocols can be used to come to consensus on various ideas or subtopic within the network. Consensus protocols use time slots where time is broken down into multiple slots, each slot having its own voting period where validators attest various proofs adding them onto their block. Generally 2/3rds of the participants need to sign off on a block for it to be added to the chain. However, the network can also choose to decide the threshold it requires for agreement. Some ideas don't need majority consensus whereas some ideas do. The network can choose to implement a "weighted" consensus mechanism where the weight of the vote is determined by the amount of stake the participant holds in the network. This is akin to the "Proof of Stake" consensus mechanism used by Ethereum. In Ethereum, the Stake is calculated in terms of "Eth". Each network can define its own currency or "standards of measurement" or choose to use their local currency as the standard of measurement. Stake in a network is generally calculated as the net value "in some currency" of assets one owns within the network.
* Messages specific to an idea/network can be routed to peers who are part or have access to networks. Some networks may be private with only certain participants having access to new knowledge within the network, some may be public, allowing anyone to connect and learn.
* One can access sub networks by connecting to a higher network along with the intention of the message. Intention is broken down into meaning using the networks schema and then routed to the right subnetwork or network peer if the peer can respond to the intention.

A codec table is generally of the following format.
Example

| name |                           tag(idea) |            code |           status |     description |
| --- | --- | --- | --- | --- |
identity|                       multihash|      0x00|           permanent|  raw binary
cidv1|                          cid|            0x01|           permanen|  CIDv1
cidv2|                          cid|            0x02|           draft|   CIDv2
cidv3|                          cid|            0x03|           draft|      CIDv3
ip4|                          multiaddr|      0x04|           permanent |
tcp|                            multiaddr|      0x06|           permanent|
sha1|                           multihash|      0x11|           permanent
sha2-256|                       multihash|      0x12|           permanent

## Core schema
<!-- 
The genesis point/origin for the projects technical specification is recorded itself as a CID. The schema of the core entities defined in this project  -->