#I Got U

I Got U is a peer to peer ledger system using cryptographically signed IOU statements.
The idea is similar to that of popular apps like Splitwise but distributed and peer to peer. 

In this you can issue an IOU saying you owe someone a specific amount of money. Currently supporting only regular currencies, but in future will support anything that the two people agree on (For e.g. I owe you 100 coconuts)


###Registration

Before you can do an IOU you have to establish a relationship with your friend. This step gets their Public Key and signing it and storing it. Ideally this should be done in a manner such that you can verify the authenticity of the public key.

####Steps Involved

1. Get the users public key through a trustable communication method (SMS, QRCode, Manual Entry - Not it does NOT involve Communication Servers)
2. Verify and sign the public key and store locally.

###Transacting

Currently the only transaction supported is requesting for and issuing IOUs. In future we will be looking at Group IOU (like Splitwise), loans, and derivatives. The steps involved are. 


####Steps Involved

0. (Optional) Alice requests for a IOU from Bob 
1. Bob creates a signed IOU, and depending on the amount and communication. For example SMS based communication uses RSA 512 and MD5 and hence is supported only for amount below the small amount limit (Rs. 100 in INR). He is free to use any of his key pairs Alice knows about.
2. Bob transfers the message to Alice without encryption in case of trustable communication methods (SMS, QRCode) or encrypted with Alice's key in case of untrustable communication methods (Email and Communication Servers)
3. Bob's device records the transaction and the signature.


