# Cost burden

Migration involves fees, primarily is the gas fee. Each transaction on ETH comes with a fee, and the fee will depend on how the[ Smart Contract ](smart-contract.md)is written.&#x20;

\
Current estimates ranges are below (calculated by MWSTW and WGV, these are lower/higher bounds, unless new options are discovered)

Note that since we are minting in independent order (not sequential 0,1,2), we have to use ERC721, **cannot use ERC721A, and there will not be gas savings for large migrations.**

| Current Gas Price (gwei) | Cost Est (1 LEP) | Cost Est \* 7000 LEPs |
| ------------------------ | ---------------- | --------------------- |
| 10 gwei                  | .0015 - .003 ETH | 10.5 ETH-21 ETH       |
| 20 gwei                  | .003 - .006 ETH  | 21 ETH-42 ETH         |
| 100 gwei                 | .015-=.03 ETH    | 105 ETH-210 ETH       |

It stands to reason that low gas is better, and perhaps we should **enforce low gas price** for migration.





## Who pays?

Simply put, it will be LEP, the community, or a combination of both.



Most likely LEP will crowdfund and that will be used for **automated reinbursement of gas on migration.** In short, in the transaction, it will estimate the gas price and transfer the same amount of ETH. The contract would be funded with sufficient ETH.
