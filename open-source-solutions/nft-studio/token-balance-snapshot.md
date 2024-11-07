# Token Balance Snapshot

The [Token Balance Snapshot](https://nft-studio.hashgraph.com/snapshot-tool/) tool allows you to capture and analyze the current distribution of tokens within a collection, helping you identify how many tokens each account holds. This is particularly useful for managing and analyzing the distribution of NFTs or fungible tokens across holders. The tool provides flexible filtering options, such as setting a minimum token amount and selecting a specific holding date or time range to analyze. This lets you create comprehensive snapshots for any set of tokens, helping you make informed decisions about community rewards, airdrops, or token management.

<table data-card-size="large" data-view="cards"><thead><tr><th align="center"></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td align="center"><a href="https://nft-studio.hashgraph.com/snapshot-tool/"><strong>Token Balance Snapshot Web App</strong> </a></td><td><a href="https://nft-studio.hashgraph.com/snapshot-tool/">https://nft-studio.hashgraph.com/snapshot-tool/</a></td><td><a href="../../.gitbook/assets/nft-studio-token-balance-snapshot-tool.png">nft-studio-token-balance-snapshot-tool.png</a></td></tr><tr><td align="center"><a href="https://github.com/hedera-dev/token-balance-snapshot"><strong>Token Balance Snapshot Code Repo</strong></a></td><td><a href="https://github.com/hedera-dev/balance-snapshot">https://github.com/hedera-dev/balance-snapshot</a></td><td><a href="../../.gitbook/assets/github-cards-icon.png">github-cards-icon.png</a></td></tr></tbody></table>

***

## How to Use the Token Balance Snapshot Tool

{% embed url="https://youtu.be/Y8NwKwny0Kc?si=47TFlRsNu0Jg6hPx" %}

### Step 1: Enter the Token ID&#x20;

We will use the [Dead Pixels Ghost Club](https://www.deadpixels.club/) ([`0.0.878200`](https://hashscan.io/mainnet/token/0.0.878200)) collection as an example for this short demo. Input the **token ID** (required) of the NFT collection to generate a snapshot of all token holders.

* **`TokenId`**: The token ID of the NFT collection.&#x20;

Apply filters to narrow down your results (optional):

* **`Min. amount`:** Specify the minimum number of tokens an account must hold.
* **`Set Date`**: Specify a start date for when accounts must have held the tokens.

Then, submit your query with **`Build List`** to return your collection's snapshot using the filters.&#x20;

<figure><img src="../../.gitbook/assets/nft-studio-token-balance-snapshot-step1.png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="info" %}
**Tips**

* Enter only the `token ID` to capture the entire list of holders without filters.
* Use minimum token amounts and holding dates to narrow down the list to active or significant holders.
{% endhint %}

### Step 2: View and Copy the Snapshot List

Choose to:

* Copy the full list of token holders.
* Copy the list with token balances included.

<figure><img src="../../.gitbook/assets/nft-studio-token-balance-snapshot.png" alt=""><figcaption></figcaption></figure>

<details>

<summary><strong>Understanding the Snapshot Results</strong></summary>

The results generated by the Token Balance Snapshot provide valuable insights into the token distribution for your specified criteria. Here's how to interpret and use them effectively:

**Account Balances & Token Holders**

* The snapshot will produce a list of Account IDs and their corresponding token balances. Each row of the list indicates an account holding tokens, along with the exact amount held.
* If you applied filters (e.g., minimum token amount, specific dates), the results will only include accounts meeting those criteria, giving you a refined view.

**Using Filters for Deeper Insights**

* By setting a higher threshold, you can focus on key stakeholders holding larger amounts of tokens.
* View how token distribution changes over time by filtering for specific dates, helping you analyze trends in holder activity and community growth.

**Export & Next Steps**

Once generated, you can export the snapshot as a CSV or other available formats. This export can then be used for:

* Import the list into an airdrop tool to distribute new tokens or NFTs to eligible holders.
* Use the data for deeper analytics on your token ecosystem to inform marketing strategies, governance decisions, or community rewards.

</details>

<details>

<summary><strong>Use Cases &#x26; Best Practices</strong> </summary>

#### **Use Cases**

* Get a detailed overview of how tokens are spread across holders and identify key accounts, such as whales, in your community.
* Use the snapshot to create a refined list of eligible accounts based on holdings, helping you distribute tokens to long-term or high-value holders.
* Identify and reward accounts that have held tokens for a specified period (e.g., 6 months), fostering community loyalty.

#### **Best Practices**

* Always verify that the correct Token ID is input to avoid errors in the snapshot.
* When filtering large collections, begin with fewer filters or smaller datasets to verify accuracy before scaling up.
* Monitor token ownership trends over time by scheduling snapshots regularly, which helps with distribution planning and community engagement tracking.
* Store exported results securely, as they contain crucial data for decision-making and token distribution.

</details>

#### 🎉 Awesome! You've obtained a comprehensive snapshot of your token holders and their balances and now completed a full tour of NFT Studio's tools!

***

## Additional Resources

* [**HashScan Network Explorer**](https://hashscan.io/)
* [**Hedera Testnet HBAR Faucet**](https://portal.hedera.com/)
* [**Dead Pixels Ghost Club Collection**](https://www.deadpixels.club/)
* [**Create and Transfer Your First Hedera NFT**](../../tutorials/token/create-and-transfer-your-first-nft.md)