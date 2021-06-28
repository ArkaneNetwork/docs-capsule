---
description: How to swap one token for another using the Wallet API
---

# Swaps

Performing a token swap consists out of 4 steps:

**Step 01:** Retrieve the token pairs that are available for swapping.

{% page-ref page="list-token-pairs.md" %}

**Step 02:** Retrieve the current exchange rate of the desired token pair.

{% page-ref page="retrieve-exchange-rate.md" %}

**Step 03:** Generate the transaction that will perform the swap

{% page-ref page="untitled.md" %}

**Step 04:** Execute the token swap, for this you can use the transfer native token request with the **`data`** parameter filled in using the one that is provided in **step 03**.

{% page-ref page="../call-a-contract.md" %}

  


