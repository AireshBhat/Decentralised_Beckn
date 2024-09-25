# Fulfilment - Tracking Protocol:

Fulfilment and Tracking of a contract involves the following functionalities.
* Ability to retrieve the contract status. Eg. Order Received, Order in Delivery, Order Fulfilled…
* Ability to track updates.
* Ability to modify an order.
* Ability to cancel an order.

## Contract Status
Relevant Peers can update the status of a contract as and when progress is logged. Conditions on who gets to update the contract can be added during the contract creation/modification. This involves required the signature of a particular address as the initiator of the update.

## Contract Tracking
Peers involved or interested in a contract can subscribe to updates by tracking the progress of a contract CID. Just as one can subscribe to events emitted by a blockchain, so can one subscribe to the events emitted during the updates of a contract.

## Order Modifications
Modifications to an order depend on whether this is allowed or not during the contract creation. The terms for modifying the order can be specified during contract creation to allow for changes in certain aspects of the contract such as status and item location. In order to modify conditions of a contract, a signed update by both the parties is mandated in order for it to be updated on the blockchain.

## Order Cancellation
A cancellation request can be raised by either party. The other party involved, on signing the request can confirm the order cancellation.