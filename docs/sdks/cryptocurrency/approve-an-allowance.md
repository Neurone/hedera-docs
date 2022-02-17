# Approve an allowance

{% hint style="info" %}
This feature is available on previewnet.
{% endhint %}

A transaction that allows a token owner to delegate a token spender to spend the specified token amount on behalf of the token owner's account. An owner can provide an allowance for hbars, non-fungible and fungible tokens. The transaction fee is paid by the owner.

* Owner: the account that owns the tokens.
* Spender: the delegate account, the account being granted the power to spend the owner’s tokens.
* Recipient: the receiver of tokens when the spender issues a `Transfer` operation.

The total number of approvals in a transaction cannot exceed 20. Note that each NFT serial number counts as a single approval, hence a transaction granting 20 serial numbers to a spender will use all of the approvals permitted for the transaction. An account can have a total of 100 allowances. Each NFT serial counts as an allowance.

**Transaction Signing Requirements**

* The transaction must be signed by the token owner's account and the account paying for the transaction fee
* If the token owner account and the transaction fee-paying account are the same only one signature is required

| **Constructor**                            | **Description**                                           |
| ------------------------------------------ | --------------------------------------------------------- |
| `new AccountAllowanceApproveTransaction()` | Initializes the AccountAllowanceApproveTransaction object |

### Methods

| **Method**                                                  | **Type**                                                                                                                | **Description**                                                                                                                                                                                                                |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `addHbarAllowance(<spenderAccountId>, <amount>)`            | [AccountId](../specialized-types.md#accountid), [Hbar](../hbars.md)                                                     | The account and amount of hbar the allowance is approved for. If `amount` is 0 the transaction will remove the `spender`’s allowance from the owner’s account, thereby freeing an allowance for future use.                    |
| `addTokenAllowance(<tokenId>,<spenderAccountId>, <amount>)` | <p><a href="../tokens/token-id.md">TokenId</a>, <br><a href="../specialized-types.md#accountid">AccountId</a>, long</p> | The  account the allowance is approved for the specified token and token amount. If `amount` is 0 the transaction will remove the `spender`’s allowance from the owner’s account, thereby freeing an allowance for future use. |
| `addTokenNftAllowance(<nftId>, <spenderAccountId>)`         | [nftId](../tokens/nft-id.md), [AccountId](../specialized-types.md#accountid)                                            | The specific NFT the spending account is approved for.                                                                                                                                                                         |
| `addAllTokenNftAllowance(<tokenId>,<spenderAccountId>)`     | [TokenId](../tokens/token-id.md), [AccountId](../specialized-types.md#accountid)                                        | The class of NFTs the spending account is approved for.                                                                                                                                                                        |

{% tabs %}
{% tab title="Java" %}
```java
//Create the transaction
AccountAllowanceApproveTransaction transaction = new AccountAllowanceAdjustTransaction()
    .addHbarAllowance(spenderAccount, Hbar.from(100));
```
{% endtab %}

{% tab title="JavaScript" %}
{% code title="" %}
```javascript
//Create the transaction
const transaction = new AccountAllowanceAdjustTransaction()
    .addHbarAllowance(spenderAccount, Hbar.from(100));
```
{% endcode %}
{% endtab %}

{% tab title="Go" %}
```go
// Some code
```
{% endtab %}
{% endtabs %}
