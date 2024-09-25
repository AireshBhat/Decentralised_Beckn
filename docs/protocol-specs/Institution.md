# Institution

## Definition
Like various departments in a factory, such as buildings, machinery, sales, production, maintenance, etc., nations also produce different departments which are called institutions. Institutions are created to fulfil the need of the Nation. Family, castes, guilds (also called trade unions), Gram Panchayats, Janapada, property, marriage, State, are all examples of institutions a nation creates to ensure the progress of social life of its citizens.

## Individual
Every individual is a limb of one or more of these institutions. A person is a member of his family as well as his community; he may also be a member of some association of his fellow professionals, if he pursues a profession. Above all, he is a member of the Nation and Society. If we consider even the larger sphere, he is a member of the whole of mankind, and then the entire universe. Truly speaking, an individual is not merely a single entity, but a plural entity. He is a part of not just one, but a number of institutions.

All institutions are interdependent, mutually complementary. There should be a sense of unity through all of them. 

> In the definition of democracy, viz. “Government of the people, by the people and for the people”; ‘of’ stands for independence; ‘by’ stands for democracy; and ‘for’ indicates Dharma. - Pandit Deendayal Upadhyay

## Decentralisation
The term decentralisation is thrown around a lot in the blockchain space. Anything implemented via a blockchain is called “decentralised”. Decentralised Finance DeFi, Decentralised Physical Infrastructure DePIn, Decentralised Autonomous Organisations, the list keeps growing. However, before we move forward, we need to keep clear what the meaning of decentralised is in our context.
By decentralisation, we mean the existence of many institutions of equal power as that of the State. By decentralisation, we mean the ability of every individual to have a direct sense of participation in the management of the goods and resources within their economy. Every institute plays a hand in the development of social life, each playing a unique role in the lives of the citizens they touch. To that effect, Decentralised Autonomous Institutions or Decentralised Autonomous Organisations are a few terms that suggest the kind of systems our tool aims to engender.

## Network
An institution that takes part in the system of production considers the 7 M’s, man, material, money, management, motive power, market and machine. In order to allow creation of complementarities between multiple networks, information regarding the 7 M’s are made public to those interacting with the network. New associations and connections can be created between networks in order to exchange the goods and services, I.e. capital, engendering diverse relationships between communities.

Every institution maintains a mapping of the peer to the role they play in advancing the aim/goal of the institution. Let us take the example of Namma Yatri, a ride hailing app built by the beckn community to understand the various peers in this institution and the role they play.

Peer 1: Developer (Skill & Ability, Market/Domain)
Peer 2: Driver (Skill, Material Provider(Automobile), Community Member, Motive Power(Human labour))
Peer 3: Executive (Management)
Peer 4: Role Certifier (Management) Can be automated using AI

**Man**: Here man represents the skill & ability of the participating individual. A peer can be a developer, driver, driver community leader, skill/ability certifier in the case of Namma Yatri.

**Material**: Easy availability of the required raw material, including the quality and properties of the raw material. In the above example, the material can be any automobile, verification machines.

**Money**: Decisions regarding how much money should be available as capital, its rate of increase/decrease, its utilisation for production, investment in assets, availability in liquid form. In the above example, this would be how the Namma Yatri community creates capital, how much each transaction is charged for using the digital network, how much they pay their contributors be it developer, community executives…

**Management**: Management of resources, human and capital. In the above example, this could be the management of drivers within a community, handling cases of support and distress. This could also be the management of resources in the various departments of the institution.

**Motive Power**: Various forms of power apart from human and animal labour such as Wind, water, steam, oil, gas, electricity and atomic power.

**Market**: Production of any particular commodity cannot be justified economically without the consideration of the market it commands.

**Machine**: A tool to fast forward production and aid the individual to increase their value output. This is created on demand while considering all the above factors. In the case of the above example, this can be the servers used to maintain network participants information, transactions carried out and the feedbacks received.

## Network Basics

- Formed around a common goal, ideal, mission - _Chiti_
- Identifies a piece of land as motherland - _Location_
- Maintains a Network Identifier(ID)
- Maintains a specification(spec) of details on how to communicate with the network peers.
- Validates network messages and maintains network sanity through security measures such as rate limiting and building measures against various attack vectors
- Maintains a record of ratings of network peers regarding various features/services offered by them.

## Technical Implementation
Each message by an identity with the network is structured in a certain way. The Beckn Protocol structures defines their “packet structure”(How data is grouped while communicating) as a pair of context and message. The context provides information/metadata regarding the message it contains, the network, location of operation, spec. It also contains the protocols the sender identity uses to communicate. The technical implementation in web3 however follows the IPNS record structure, adding on to it a few parameters such as network ID, location and action.

Example of a record comparing the Beckn message structure and how the data is encoded in an IPNS Record. Future protocols will assume this packet structure and will mention any additional keys to be added.
Context[1](%20https://developers.becknprotocol.io/docs/core-specification/schema-reference/contextforsearch):

|                 |                                                                                                                 |                                                                                                                                        |
| --------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Field**       | **Type**                                                                                                        | **Description**                                                                                                                        |
| domain          | string                                                                                                          | Describes the domain of an object                                                                                                      |
| country         | [Country/properties/code](https://developers.becknprotocol.io/docs/core-specification/schema-reference/country) | Country code                                                                                                                           |
| city            | [City/properties/code](https://developers.becknprotocol.io/docs/core-specification/schema-reference/city)       | City code                                                                                                                              |
| action          | string                                                                                                          | Defines the Beckn API call. Any actions other than the ennumerated actions are not supported by Beckn Protocol Allowed values : search |
| core\_version   | string                                                                                                          | Version of Beckn core API specification being used                                                                                     |
| bap\_id         | string                                                                                                          | Unique id of the BAP.                                                                                                                  |
| bap\_uri        | string                                                                                                          | URI of the BAP for accepting callbacks.                                                                                                |
| bpp\_id         | string                                                                                                          | Unique id of the BPP.                                                                                                                  |
| bpp\_uri        | string                                                                                                          | URI of the BPP.                                                                                                                        |
| transaction\_id | string                                                                                                          | This is a unique value which persists across all API calls from search through confirm                                                 |
| message\_id     | string                                                                                                          | This is a unique value which persists during a request / callback cycle                                                                |
| timestamp       | string                                                                                                          | Time of request generation                                                                                                             |
| key             | string                                                                                                          | The encryption public key of the sender                                                                                                |
| ttl             | string                                                                                                          | The duration after timestamp for which this message holds valid                                                                        |


IPNS Record[2](%20https://specs.ipfs.tech/ipns/ipns-record/):

|                 |          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| --------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Field**       | **Type** | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Value           | bytes    | It can be any content path, such as a /ipns/{ipns-key} path to another IPNS record, a [DNSLink](https://dnslink.dev/) path (/ipns/example.com) or an immutable IPFS path (/ipfs/baf...). Implementations must include this value inside the DAG-CBOR document in IpnsEntry.data[Value].                                                                                                                                                                                                                                              |
| Validity Type   | uint64   | Defines the conditions under which the record is valid. The only supported value is 0, which indicates the validity field contains the expiration date after which the IPNS record becomes invalid. Implementations must support ValidityType = 0 and include this value inside the DAG-CBOR document at IpnsEntry.data[ValidityType].                                                                                                                                                                                               |
| Validity        | bytes    | Expiration date of the record with nanoseconds precision. Expiration time should match the publishing medium's window.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sequence        | uint64   | Represents the current version of the record (starts at 0). Implementations must include this value in inside the DAG-CBOR document at IpnsEntry.data[Sequence].                                                                                                                                                                                                                                                                                                                                                                     |
| TTL             | uint64   | A hint for how long (in nanoseconds) the record should be cached before going back to, for instance the DHT, in order to check if it has been updated. The function and trade-offs of this value are analogous to the TTL of DNS record. Implementations must include this value inside the DAG-CBOR document at IpnsEntry.data[TTL].                                                                                                                                                                                                |
| Public Key      | bytes    | Public key used to sign this record. If public key is small enough to fit in IPNS name (e.g., Ed25519 keys inlined using identity multihash), IpnsEntry.pubKey field is redundant and may be skipped to save space. The public key must be included if it cannot be extracted from the IPNS name (e.g., legacy RSA keys). Implementers must follow key serialization defined in [PeerID specs](https://github.com/libp2p/specs/blob/master/peer-ids/peer-ids.md#key-types). List of supported key types listed in IPNS Keys section. |
| Signature       | bytes    | Provides the cryptographic proof that the IPNS record was created by the owner of the private key. Implementations must include this value in IpnsEntry.signatureV2 and follow signature creation and verification as described in Record Creation and Record Verification.                                                                                                                                                                                                                                                          |
| Extensible Data | DAG-CBOR | Extensible record data in [DAG-CBOR](https://ipld.io/specs/codecs/dag-cbor/spec/) format. **Extra fields related to the beckn protocol will be added here**.                                                                                                                                                                                                                                                                                                                                                                         |

As mentioned in the above table, extra data related to beckn such as the network location, network ID, network spec version and action are added in a DAG-CBOR[3](https://ipld.io/specs/codecs/dag-cbor/spec/) encoded format to be interoperable with the IPFS network.

|                    |          |                                                                                                                |
| ------------------ | -------- | -------------------------------------------------------------------------------------------------------------- |
| **Field**          | **Type** | **Description**                                                                                                |
| Network ID         | CID      | Substrate chain spec ID                                                                                        |
| Network Location   | bytes    | Motherland/Location of the network                                                                             |
| Beckn Spec Version | bytes    | Version of Beckn core API specification being used                                                             |
| Action             | bytes    | Defines the Beckn API call. Any actions other than the ennumerated actions are not supported by Beckn Protocol |


	message NetworkEntry {
	 optional bytes pubKey = 7;
	 optional bytes signatureV2 = 8;
	 optional bytes data = 9;
	}

	// NetworkEntry.data
	{
	  Sequence: …
	  TTL: …
	  Validity: …
	  ValidityType: …
	  Value: …
	  ExtensibleData: …
	}

	// NetworkEntry.data.ExtensibleData
	{
	  NetworkID: …
	  NetworkLocation: …
	  BecknSpecVersion: …
	  Action: …
	}
