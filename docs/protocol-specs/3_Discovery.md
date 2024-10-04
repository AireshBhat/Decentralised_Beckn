# Discovery Protocol

The discovery protocol is used to discover peers within an institution. The network maintains records of all its peers and the various roles they play in advancing the institutions aim/goal.
Discovery protocol in the beckn protocol involves implementing the search/on\_search APIs by the network provider and consumer respectively. Hence a message containing data pertaining to search will have the enum `SEARCH` for the field `Action` and `ON_SEARCH` for data pertaining to on\_search.

A discovery protocol is a set of processes a network follows in order to identify the relevant peers within the network. Some amount of personal data is shared by the peer with the network, eg. location, age, relationship, qualification. This allows the network to be able to direct requests to the peers who may potentially be able to serve them.

The blockchain database maintains a mapping of PeerID to the service they provided. However, for information that may change frequently, eg current location, online availability, the network may implement a Distributed Hash Table(DHT) to track such ephemeral information.

A DHT is table that stores a key value pair in each entry. In the case of IPFS, the key is the PeerID and the value is the ContentIdentifier(CID). Similarly BitTorrent uses a DHT to identify which peer is storing which file and share files without needing a central tracker. In the discovery protocol, nodes maintain a DHT according to the specifications of the network. This allows the network to identify which peer to direct the request to.
In the case of mobility, the DHT could store the mapping of PeerID(which would be the drivers) to the [Geospatial Index (H3)](https://h3geo.org). This would allow the network to pass on the PeerIDs of those who are present in a particular area. 

