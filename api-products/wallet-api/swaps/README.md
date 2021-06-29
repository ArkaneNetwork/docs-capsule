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

{% page-ref page="build-swap-tx.md" %}

**Step 04:** Execute the token swap, for this you will need to take the response from **step 03** and launch transactions accordingly.

{% page-ref page="../transfer-a-native-token.md" %}



  


