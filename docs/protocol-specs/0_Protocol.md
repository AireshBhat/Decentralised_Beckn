## Origin of the protocol. [TODO: Fill in its relation to your identity and past, to be filled by others and linked here]

Decentralisation and Swadeshi are two terms that define the foundations of the protocol. Decentralisation means the ability of an individual to have a direct sense of participation in the management of the resources and capital of the network they are a part of. Using latest technological tools like blockchain for protocol evolution and AI for language support, anyone can now take part in capital management and help in maintaining social life and eventually surpassing it by contributing to national or international goals. Decentralisation is in response to the current centralised economic structure which engenders monopolisation of commodities. In the olden days of Bharat, there existed multiple institutions of equal power to the state that helped maintain social life. Trades and associations between these institutes were not interfered with by the State unless requested. Blockchain smart contracts help maintain a digital record of these trades and associations allowing for easy governance of the network and reducing the need for State intervention in every matter. AI can help articulate the intents of participants and service providers allowing us to easily locate or connect individuals that can serve each others needs.
Every nation houses a national soul. This soul manifests itself in the form of the culture, the language, the customs and the traditions of its people. These customs and traditions heavily influence our social interactions and economic structures. Current blockchain implementations come with an underlying economic structure that does not suit the national genius. An economic structure that is Swadeshi aims to achieve the following objectives and goals.
1. An assurance of the minimum standard of living to every individual and preparedness for the defence of the Nation.
2. Further increase above this minimum standard of living whereby the individual and the Nation acquire the means to contribute to world progress on the bases of its own Chiti(Soul Identity)
3. To provide meaningful employment to every able-bodied citizen, by which the above two objectives can be realised, and to avoid waste and extravagance in utilising natural resources.
4. To develop machines suited to Bharatiya conditions, taking note of the availability and nature of the various factors of production (Seven M's).
5. This system must help, and not disregard the human being - the individual. It must protect the cultural and other values of life. This is a requirement which cannot be violated except at the risk of great peril.
6. The ownership, state, private or any other form, of various industries must be decided on a pragmatic and practical basis.

## What are the innovative or preserving intentions of the protocol?
or in other words, What aspects of the protocol orient it towards the future and what aspects orient it towards the past?

The protocol acts as a tool to help bring nature to culture. Chiti, the Spirit Identity is used to describe the innate nature of that identity. Chiti once defined, becomes the standard of measurement for an individual. Whatever is in alignment with ones Chiti is added onto the identity, this ends up describing the culture of the identity. The identity is not however always singular, the individual 'I' is inseperable related to the plural 'We'. The society. Each group of individuals that constitute communities, institutions, State, a brand identity, has an innate nature of its own. A group mind you can call it. Chiti is the touchstone on which each action, each attitude is tested, and determined to be acceptable or otherwise. In blockchain terms, Chiti acts as the validator to what becomes part of the groups culture.

## What is the role of duration & repititiveness in the protocol?
>It is the protocol itself that creates a sense of time

Blockchain consensus engines such as Polkadots' BABE + GRANDPA protocol provide a sense of time to the participants network.
BABE (Blind Assignment for Blockchain Extension) and GRANDPA (GHOST-based Recursive Ancestor Deriving Prefix Agreement) are two complementary protocols used by Polkadot to achieve consensus on its blockchain network.

BABE is the block production mechanism. It assigns block creation slots to validators in a randomized but weighted manner, ensuring a fair and decentralized block generation process. Validators take turns producing blocks in a sequence, which helps maintain a steady flow of new blocks on the chain.
GRANDPA is the finality gadget. It provides a method for validators to agree on the final state of the blockchain, allowing for rapid confirmation of blocks. Even if the network experiences temporary forks, GRANDPA can finalize blocks by having validators vote on the longest chain, ensuring that once a block is finalized, it cannot be reverted.
Together, BABE and GRANDPA enable Polkadot to achieve both fast block production and strong finality guarantees, enhancing the network's scalability and security.

Here blockspace acts as a reserviour of culture. It is also used in future processes to help shape the outcome as a form of feedback mechanism.

## What is the vision of a future beyond the protocol?
The vision of the project is to help aid establish Dharma. Here Dharma can be loosely translated in English to "intrinsic responsibility". 
>“Intrinsic responsibility” means that the system is designed to send feedback about the consequences of decision making directly and quickly and compellingly to the decision makers. - Donella Medows, Systems Thinking

The vision of the protocol is to provide a tool for systems to help instill intrinsic responsibility within its citizens. This may initially require the usage of heavy technology in order to bring current systems in order, however, I believe...
> The conquest of the emotions and the intellect by the spirit is the work of the future. - Sri Aurobindo

Hence, I envision a future where technology is used only to communicate these feelings/emotions with each other in a transparent manner rather than being the means to an end themselves(AI robots that replace humans). We believe that machines are tools that aid human beings. If machines created replace humans, the entire purpose of building the machine is lost. Machines are created for the purpose of evolving humanity, not in replacing it.

## What is the definition of the protocol?
A tool for systems to help instill intrinsic responsibility within its citizens.

## How is the protocol structured?
The protocol is comprised of many sub protocols, each of which is designed to help the network participants interact with each other in a fair and just manner. 
* The Data protocol, how each network structures their message packets and how each network stores data pertaining to the network and to the participants is provided in the [1_Data.md](./1_Data.md) file.
* General structure of the data each network must maintain as part of the protocol and the logic behind them is provided in the [1_Institution.md](./1_Institution.md) file.
* Every network must provide the basic tools to its citizens to maintain their "digital identity". The process of onboarding a new user and the protocols for creating a digital identity for them is provided in the [2_Onboarding.md](./2_Onboarding.md) file.
* Every network defines a DHT table, similar to a DNS table which maps the IP address of a server to a "url" of a network providing data using the HTML protocol. This allows external participants to find peers within the network that can potentially provide the service they are looking for. The protocol for maintaining this DHT table to discover network peers and their services is provided in the [3_Discovery.md](./3_Discovery.md) file.
* Every network constructs rules and regulations based on their aim or goal, formally called Chiti. These rules and regulations can change as the network evolves. Contracts/Interactions created by network peers are checked basis these rules and regulations and are added to the network blockchain if they satisfy the Chiti. The protocol for maintaining the Chiti and the rules and regulations of the network is provided in the [4_ContractCreation.md](./4_ContractCreation.md) file.
* Fulfillment and Tracking of the contract and its closure is provided in the [5_FulfillmentTracking.md](./5_FulfilmentTracking.md) file. These additional rules are defined during contract creation and are used to determine the success or failure of the contract. Each contract could be thought of as a new branch of a git repository. Once fulfilled, the contract is merged into the main branch of the network blockchain, highlighting the contribution towards the progress of the networks aim/goal.
* Rating and feedback play a crucial role in the feedback mechanism of the network. To determine whether the actions being taken by the network peers are actually advancing the aims/goals of the network, rating and feedback is requested from the network participants. Interactions and contracts are rated allowing the network to fairly determine the efficacy of a product/service. The protocol for maintaining the rating and feedback of the network participants is provided in the [6_RatingFeedback.md](./6_RatingFeedback.md) file.