A decentralised implementation of the *[beckn protocol](https://developers.becknprotocol.io/docs/introduction/introduction/)*

## What is a protocol?
Protocols serve as tools or systems to facilitate coordinated behaviour. Our entire social setting is comprised of protocols, whether we like them or not. For example, the protocol of driving on the right side of the road, the protocol of standing in a queue, the protocol of shaking hands, the protocol of saying "thank you" and "please". Some protocols are enforced by a central authority like a national government body, some are social customs we follow, some emerge in times of emergency need, for. eg the social distancing protocol during the COVID-19 pandemic.

Nations or institutions create protocols in order to enhance the efficiency of the organisation towards achieving its aims/goals. Protocols are created with the goal of enhancing the efficiency of self-organisation within a community.

There are two main aspects of protocols according to [Olivia Steiert](),
* **Simultaneous enablement & restraint**: Protocols enable certain behaviours while restraining others. For example, the protocol of driving on the right side of the road enables the smooth flow of traffic while restraining the chaos that would ensue if everyone drove on the side of the road they wanted to.
* Inherent temporality: Protocols exist within the "realm of time". They are intinsically process oriented.

Protocols can evolve over time through feedback. Protocols inflict certain behaviours in people that cannot be guessed during its inception. Understanding these behaviours and adopting changes to the protocol can help a community/organisation to achieve its goals more efficiently. In a way, its a form of self-organisation.

Enacting the protocol over and over again tend to become ends in themselves. This may lead to enactment of certain behaviours that may actually be harmful to the community. For eg. The idea of capitalists to focus on profits over ecology has become a business protocol which is very evident in the way they speak. An economic society must have ideals or goals that tend to the evolution of all aspects of the human being. Body, mind, intellect and soul. Protocols that emerge under such ideals are more likely to be beneficial to the community. Hence, the vision/ideals of a network is highly critical in being able to know whether a protocol is truly serving its purpose or not.

> Protocolization links past & present to future similar to how Experience is linked to expectation.

Similarly, the beckn protocol is a protocol that is designed to facilitate the exchange of goods and services in a decentralised manner. The protocol is designed to be open source and is maintained by the beckn community. The protocol is designed to be implemented by any individual or organisation that wishes to facilitate the exchange of goods and services. Todays digital world provides access to even the remote parts of the world. This feature of technology can be used to provide information regarding institutions and their intentions in developing society clearer and more transparent to its citizens.

A truly decentralised technical application is one where individuals have control over their data and understand their power within the networks they are a part of. Decentralisation is a term used to describe the economic structure which we aim to build as compared to todays centralised economic structure which engenders Monopolisation of commodities. Decentralisation of power provides a direct sense of participation to the user in the management of the resources and capital of the network they are a part of. More details on what inspires our economic structure can be found in the [Integral Humanism](https://deendayalupadhyay.org/images/book/Booklet%20on%20IntegralHumanism.pdf?ref=quillette.com) philosophy written by Pandit Deendayal Upadhyay. This is a replacement to the current economic structures such as Capitalism, Socialism, Communism and various other philosophies which dictates the workings of our society today.

Identity of the organisation plays a key role in achieving self-organisation [Intersectional Social Data -RadicalXChange](https://www.radicalxchange.org/media/blog/2019-10-24-uh78r5/). 

# Backend
Data management is planned to be implemented using the [Willow Protocol](https://willowprotocol.org/specs/index.html#specifications). Networks implement the Willow protocol to manage the data of the network participants. Blockchains are used similar to how users post data on social media. Data that the user wishes to be discovered by the public are stored on their identity blockchain. Similarly, networks store transaction contracts on their network blockchains. The network defines the schema and the rules participants are to follow in order to transact with their peers. 
The Blockchain is implemented using the Substrate sdk. Substrate sdk allows for custom runtime logic. There are currently two types of substrate runtimes:
1. Identity Chain: A chain run by each individual that houses their identity. It maintains identity data such as their features, their attributes, their Verifiable Credentials and other details that pertain to them. Please refer to the [Intersectional Social Data(ISD) protocol](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3375436) to have a deeper understanding of how we model an Identity within a network.
2. Network Chain: A chain that is maintained by the participants of the network. Each network is modelled around their aim or goal. Each identity enacts a certain role within the network in order to advance the networks aim or goal. The network stores smart contracts of transactions by the network participants with other peers. These contracts maintain the data of the transaction, the terms of the transaction, the fulfilment of the transaction and the corresponding feedback and rating. This information can further be used to understand whether the network is progressing towards its goals or not.

Further details on the protocol can be found in the [protocol-specs](./docs/protocol-specs) folder.

# Frontend
Frontend will mostly be dApps that individuals can download and run on their chains along with the UI written in React. Work on this will be started soon...