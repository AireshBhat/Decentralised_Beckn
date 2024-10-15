# Institution

## Definition
Like various departments in a factory, such as buildings, machinery, sales, production, maintenance, etc., nations also produce different departments which are called institutions. Institutions are created to fulfil the need of the Nation. Family, castes, guilds (also called trade unions), Gram Panchayats, Janapada, property, marriage, State, are all examples of institutions a nation creates to ensure the progress of social life of its citizens.

## Individual
Every individual is a limb of one or more of these institutions. A person is a member of his family as well as his community; he may also be a member of some association of his fellow professionals, if he pursues a profession. Above all, he is a member of the Nation and Society. If we consider even the larger sphere, he is a member of the whole of mankind, and then the entire universe. Truly speaking, an individual is not merely a single entity, but a plural entity. He is a part of not just one, but a number of institutions.

All institutions are interdependent, mutually complementary. There should be a sense of unity through all of them. 

> In the definition of democracy, viz. “Government of the people, by the people and for the people”; ‘of’ stands for independence; ‘by’ stands for democracy; and ‘for’ indicates Dharma. - Pandit Deendayal Upadhyay

## Network
An institution that takes part in the system of production considers the 7 M’s, man, material, money, management, motive power, market and machine. In order to allow creation of complementarities between multiple networks, information regarding the 7 M’s are made public to those interacting with the network. New associations and connections can be created between networks in order to exchange the goods and services, I.e. capital, engendering diverse relationships between communities.

Every institution maintains a mapping of the peer to the role they play in advancing the aim/goal of the institution. Let us take the example of Namma Yatri, a ride hailing app built by the beckn community to understand the various peers in this institution and the role they play.

**Peer 1**: Developer (Skill & Ability, Market/Domain),

**Peer 2**: Driver (Skill, Material Provider(Automobile), Community Member, Motive Power(Human labour)),

**Peer 3**: Executive (Management),

**Peer 4**: Role Certifier (Management) Can be automated using AI 

---

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
The entire network is identity centric. The network is made up of a group of individuals that maintain an identity. The above definitions make up the DNA of an institution. The network is comprised of the following components:
```rust
pub struct NetworkDef {
    /// The name of the network.
    pub name: String,

    /// Modifiers of this network - the network seed, properties and origin time.
    ///  The modifiers are included in the DNA hash
    /// computation.
    pub modifiers: NetworkModifiers,

    /// A vector of zomes associated with your DNA.
    pub integrity_schema: IntegrityZomes,

    /// A vector of zomes that do not affect
    /// the [`DnaHash`].
    pub coordinator_schema: CoordinatorZomes,

    /// A list of past "ancestors" of this network.
    ///
    /// Whenever a network is created which is intended to be used as a migration from
    /// a previous network, the lineage should be updated to include the hash of the
    /// network being migrated from. Network hashes may also be removed from this list if
    /// it is desired to remove them from the lineage.
    ///
    /// The meaning of the "ancestor" relationship is as follows:
    /// - For any network, there is a migration path from any of its ancestors to itself.
    /// - When an app depends on a NetworkHash via UseExisting, it means that any installed
    ///     network in the lineage which contains that NetworkHash can be used.
    /// - The app's Coordinator interface is expected to be compatible across the lineage.
    ///     (Though this cannot be enforced, since Coordinators can be swapped out at
    ///      will by the user, the intention is still there.)
    ///
    /// The software itself does nothing to ensure the correctness of the lineage, it is up to
    /// the app developer to make the necessary guarantees.
    pub lineage: HashSet<DnaHash>,
}

pub struct NetworkModifiers {
    /// The network seed of a network is included in the computation of the network hash.
    /// The network hash in turn determines the network peers and the DHT, meaning
    /// that only peers with the same network hash of a shared network participate in the
    /// same network and co-create the DHT. To create a separate DHT for the network,
    /// a unique network seed can be specified.
    pub network_seed: NetworkSeed,

    /// Any arbitrary application properties can be included in this object.
    pub properties: SerializedBytes,

    /// The time used to denote the origin of the network, used to calculate
    /// time windows during gossip.
    /// All Action timestamps must come after this time.
    pub genesis_time: Timestamp,
}

pub type NetworkSeed = String;

enum Component {
    Unencrypted(ComponentData),
    Encrypted {
        algorithm: EncryptionAlgorithmId,
        key_id: [u8; 32],
        encrypted_data: Vec<u8>,
    }
}

struct ComponentData {
    schema: SchemaId,
    data: Vec<u8>,
}
```