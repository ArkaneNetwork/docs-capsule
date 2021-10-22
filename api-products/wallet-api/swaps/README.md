---
description: How to swap one token for another using the Wallet API
---

# Swaps

Performing a token swap consists out of 4 steps:

**Step 01: **Retrieve the token pairs that are available for swapping.

{% content-ref url="list-token-pairs.md" %}
[list-token-pairs.md](list-token-pairs.md)
{% endcontent-ref %}

**Step 02:** Retrieve the current exchange rate of the desired token pair.

{% content-ref url="retrieve-exchange-rate.md" %}
[retrieve-exchange-rate.md](retrieve-exchange-rate.md)
{% endcontent-ref %}

**Step 03:** Generate the transaction that will perform the swap

{% content-ref url="build-swap-tx.md" %}
[build-swap-tx.md](build-swap-tx.md)
{% endcontent-ref %}

**Step 04:** Execute the token swap, for this you will need to take the response from **step 03** and launch transactions accordingly.

{% content-ref url="../transfer-a-native-token.md" %}
[transfer-a-native-token.md](../transfer-a-native-token.md)
{% endcontent-ref %}



\
