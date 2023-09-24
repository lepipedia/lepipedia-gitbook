# Process overview

1. [https://opensea.io/collection/blockchainsurvivalkit](https://opensea.io/collection/blockchainsurvivalkit)Get LEP art/names
   1. This can be retrieved with the OpenSea API. [Code is here](https://github.com/KenTheWhaleGoddess/LowEffortPunks/tree/main/get-lep-data), request access to repo.
      1. This returns a list where each LEP is an item in the list..\
         `{`\
         `"identifier":"87198930750286842836902562062466327909054195361095182156017579399890411192321", #OS token ID`\
         `"name":"low effort punk 6785", #use name to get new ID`\
         `"image_url":"https://i.seadn.io/gcs/files/f039f1fe6e255bdbf29e0f587417789b.png",`\
         `"created_at":"2023-07-05T20:30:30.225489",` \
         `"description":null #most are null, but some have descriptions`\
         `}`
   2. Pin the art on IPFS (Download from `image_url` above)
   3. Pin the metadata on IPFS (name, description & image mainly)
   4. Test/deploy contracts (after there is consensus on that...) [Code is here](https://github.com/KenTheWhaleGoddess/LowEffortPunks/tree/main), same repo as 1. Check [smart-contract.md](smart-contract.md "mention") Section on open questions.





We will do this for each of the LEP collections...

* Low Effort Punks [https://opensea.io/collection/low-effort-punks](https://opensea.io/collection/low-effort-punks)
* Blockchain Survival Kit [https://opensea.io/collection/blockchainsurvivalkit](https://opensea.io/collection/blockchainsurvivalkit)
* Words by LEP [https://opensea.io/collection/wordsbylep](https://opensea.io/collection/wordsbylep)
* LEP Epic Stuff [https://opensea.io/collection/lep-epic-stuff](https://opensea.io/collection/lep-epic-stuff)
* LEP Exclusives [https://opensea.io/collection/lep-exclusives](https://opensea.io/collection/lep-exclusives)
