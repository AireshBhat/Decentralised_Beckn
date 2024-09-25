# Onboarding Protocol - v0.1

## Identity Creation

Maintaining a digital identity is the responsibility of the individual. Maintaining
data that describes the user, their features, their likes and dislikes, their real
world actions is handled by the big tech companies of today. This gives them
the advantage to sell the identity for profits. Maintaining our identity in todays
digital world will give us the ability to shape how capital is formed and
distributed within our networks and societies allowing for the creation of truly
decentralised economies.

# Devices
![Server](https://github.com/user-attachments/assets/67eca586-b692-4466-83fc-ef54493856d6)
Server (Full Node)
![Laptop](https://github.com/user-attachments/assets/e396a4e6-3c91-4b1d-ad51-a1722169e97a)
Laptop (Full Node/Light node)
![Mobile](https://github.com/user-attachments/assets/02406526-f023-44e1-b42d-0473563ca811)
Smart Phone/Mobile (Light Node) 
Each Device acts as a Node for an identity. The node either houses data about
the identity or are access points for the user to interact with the data. Each
node also acts as a “Relay Server” for the networks they are a part of. Just as
how a server running the TCP/IP protocol allows all internet messages to pass
through it, each node allows all Network related messages to pass through it.
This is useful for when network participants need to find network data or other
peers from the network.

### Full Node
- Houses core identity data. Each Identity is a blockchain managed by a public key that is used to sign the changes of the identity.
- Registers light nodes that communicate through it.
- Displays identity information, schemas and protocols used to interact with identity
- Network Data is stored in an IPFS(Inter Planetary File System) manner, utilising the CID(Content Identifier) concept to identify data basis their content.
### Light Node
- Access points for the user to operate their identity
- Cache data for easy redistribution
- Normally uses some form of biometric verification to authenticate the user.

The Onboarding protocol is a protocol for networks to implement in order to
onboard a user into the decentralised network. A decentralised network, is a network that has its own soul, an institution that spawns organically as and when required in order to progress the aim/goal of the nation.
Processes
1. Installing the Required Open Sourced Software
2. Spawning a blockchain identity
3. Creating connections to networks and other identities

#### **Installing Open Sourced Software**
The Open Sourced Software is a software product that implements a blockchain to house the data of an identity. A blockchain is by itself a protocol for maintaining data where each new entry references its previous entry in order maintain an ever increasing connection of data. However, storing information alone doesn’t create trust. Information must also be verified by relevant parties. This step forms the consensus mechanism of the blockchain providing guarantees to the source of information. Every network that aims to be decentralised must encourage its participants to store their identities using these protocols in order to avoid the responsibility of maintaining the data themselves. A user can install the software from any network they deem safe.

#### **Spawning blockchain identities**
Once the required software is downloaded, the user can create a new digital identity by spawning a new blockchain and define the operating conditions, connect light nodes that can be used to operate the identity.
Each identity is its own main chain. Since the blockchain is implemented using
the substrate framework, each identity can be called as the relay chain. The
Parachains or Sidechains are spawned by the main relay chain as and when
contracts are created between parties involved.

#### **Managing attributes and proofs**
Identities manage attributes (Gunas) of an attribute themselves. When providing a service on a network, these attributes are rated by the customers basis the contract they create.
