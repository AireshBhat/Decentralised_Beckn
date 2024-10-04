# Rating and Feedback Protocol:

Feedback/Rating may be requested by either party regarding attributes of their identity in relation to the contract served. This can help strengthen the evidence of an attribute of an identity leading to higher trust.

The rating once provided can be hashed and submitted to the contract as proof of rating. The rating can be encrypted to make it private. The identity may chose to provide access of the public key to those who need to access the rating.

### Feedback request message schema
	{
	  ContractCID: Bytes
	  IdentityAttributes: Attribute[] \\ The list of attributes the identity seeks rating for
	}

_The attributes of an identity can also be called as ‘Gunas’_