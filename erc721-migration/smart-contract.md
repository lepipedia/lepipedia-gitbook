# Smart Contract

WGV curernt Smart Contract code here -- [https://github.com/KenTheWhaleGoddess/LowEffortPunks/tree/main](https://github.com/KenTheWhaleGoddess/LowEffortPunks/tree/main)



\
\# Requirements

* Use onERC1155Received. [https://github.com/KenTheWhaleGoddess/LowEffortPunks/blob/main/LowEffortPunks.sol#L44-L61](https://github.com/KenTheWhaleGoddess/LowEffortPunks/blob/main/LowEffortPunks.sol#L44-L61)
  * Burn/mint in same tx
* ERC721 with metadata
* 2 smart contracts, "Flexible Renderer" which can be modified for new art/fully on-chain

## TBD

* Gas refund -- ETH trasnfered to the migrator (if i migrate 2 leps, it estimates the gas and sends the same ETH back)&#x20;
* Roles? So WGV/Other can help LEP manage the contract.
  * What powers should WGV/Other have?
* LEP can "force mint"? **People not in favor of this, seems too strong**
  * Eg. we know of certain "lost wallets" from community members. Can LEP simply mint those without access to the original?
  * Might go against some principles of crypto (LamboWhale brought up that its a strong ability)
  * Time bound (can only request for 6mo after contract is deployed, then the function is locked?)
* Can the OG LEP be retrieved? **No , see above**
  * It has some provenance value
  * Would complicate the "force mint" if the original is unretrievable&#x20;
* How will the mapping from old/new LEP be stored? **New LEPs will have old large OS token IDs, new LEPs will have the final OS token id ++. This is simpler and less gas than prev options**
  * Server with ECDSA signature?
  * Can a Merkle tree be used?
  * on-chain mapping is the simplest (currently in WGV code above), but will be another large gas cost...
* Do we even do burn to mint? Or do some airdrop of tokens? **Burn to mint with two directions?**&#x20;
  * Airdrop makes OG LEP value confusing/negligible
  * Burn to Mint leaves 2 collections forever, which is also confusing&#x20;
  * Either way the goal is that holders arent paying excess gas through the process.&#x20;
  * turn off non safeTransfer in the ERC721.

