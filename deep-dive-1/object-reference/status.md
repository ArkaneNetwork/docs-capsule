---
description: A concept that is available in the Market API
---

# Status

An offer has a status and throughout the lifecycle of an offer, it will pass through several statuses. 

### NEW

The first status in the lifecycle of an offer. This is the status a newly created offer receives. The offer is not yet live it is waiting for the Approval transaction and the signed data. Consider this the state where a 3rd party platform asks to create a certain offer. The market will create the core concept for the offer and is now waiting for it to be finalized, by updating the offer with 

* the transaction hash of the Approve call 
* the signed data, confirming to the market that the NFT can be taken into custody.

### INITIATING\_OFFER

Once the offer is updated with the transaction hash of the Approve call and the signed data, the offer will move from state **NEW** to state **INITIATING\_OFFER**, and the market will try to take the NFT into custody.

### READY

The READY status means that the NFT has been successfully taken into custody and that the offer is live. Ready the be bought, bid on, or canceled. 

### **FINALIZING\_OFFER**

When the lifecycle of an offer is coming to an end, this can be triggered by a sale of the NFT, by canceling the sale, or in case of an auction, when time runs out, the state moves from **READY** to **FINALIZING\_OFFER**. This means the NFT is moving out of custody and is either being sent to the wallet of the buyer or back to the wallet of the seller.

### SOLD

The **SOLD** state is a final state, which follows the **FINALIZING\_OFFER** state. The transition happens when the offer was sold and the NFT was successfully moved out of custody and moved into the buyer's wallet. 

### CLOSED

The **CLOSED** state is a final state, which follows the **FINALIZING\_OFFER** state. The transition happens when the offer was canceled by the seller and the NFT was successfully moved out of custody and moved back into the seller's wallet.

