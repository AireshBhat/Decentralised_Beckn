# Contract creation protocol

These messages are passed directly from peer to peer, passing through the network relay servers. Every node acts as a relay server. Full nodes implement rate limiting and signature checks to maintain the sanity of the network. Nodes maintain ledgers of interactions with other peers. This information is used to ensure participates maintain a balance in sending and receiving, similar to how IPFS manages relationships between their nodes[1](https://arxiv.org/abs/1407.3561). This ledger also helps in passing on the message to the right network the peer is a part of.

	type Ledger struct {
		owner      NodeId
	    partner    NodeId
	    bytes_sent int
	    bytes_recv int
	    timestamp  Timestamp
	    nonce      int
		networkID  bytes[] // Networks the partner is a part of
	}

The final contract between the two participants is a signed document containing the terms of business. This document generally contains the IDs of the two participants, the conditions under which the contract is signed, how one contract fulfilled the terms of service, how the payment was made and in what form. Both the participants sign the contract. The peer then submits the signed contract to the network to store on the blockchain which acts as a storage of proof. Before adding the contract to the network chain, the network participants verify the details and the proofs provided by the peer. For eg, signature checks of the peers, contract conditions, verify validation proofs that the network requires (mirrors the process of KYC). The customer identity may choose to store the CID details of the transaction or contract in order to use them as a means of verification in future processes.

![Contract Creation](https://github.com/user-attachments/assets/e5c38392-6d69-4834-b445-23b8d183e641)

The contract creation protocol in the beckn protocol follows three steps, select, init and confirm. The first step select is responsible in choosing the required services and notifying the peer. The second step is responsible in agreeing on the terms of fulfilment for either of the parties. The third and final step creates and binds the contract between the two participants. The contract is stored on the networks blockchain by the peer in order to create an immutable proof of the contract terms.

### Final Contract schema
The schema for the contract follows the beckn schema for the `on\_confirm` message. The full schema can be found [here](https://developers.becknprotocol.io/docs/core-specification/schema-reference/order).
	{
	  order_id:    OrderID
	  order_state: bytes
	  items:       Item[]
	  add_ons:     AddOns[]
	  offers:      Offers[]
	  billing:     Billing
	  fulfillment: Fulfillment
	  quote:       Quote
	  payment:     Payment
	  created_at:  Date
	  updated_at:  Date
	}

