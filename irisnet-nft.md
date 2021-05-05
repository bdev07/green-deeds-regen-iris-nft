# Green Deeds NFT Issue on IRISnet

This project provides proof of concept for Green Deeds NFT badges on a local IRISnet test node.  It's meant to assist our proposal submission for the gitcoin Green NFT hackathon.  It is not meant as a walkthrough for recreation.  

First, follow the [getting started](https://www.irisnet.org/docs/get-started/install.html#install-go) guide to install ````iris```` and utilize their [NFT](https://www.irisnet.org/docs/cli-client/nft.html#available-commands) feature.  

Then create ````meta.json```` files for each level of badge.  The schema will follow the layout described in the [NFT](https://www.irisnet.org/docs/cli-client/nft.html#available-commands) module. 

````bash
# issue-badges.sh
# Issue level one badge
iris tx nft issue greendeedlevel1 --from=britt-iris-key --name=green-deeds-level-one --schema=level-one-meta.json --chain-id=green-deeds-test

# Issue level two badge
iris tx nft issue greendeedlevel2 --from=britt-iris-key --name=green-deeds-level-two --schema=level-two-meta.json --chain-id=green-deeds-test

# Issue level three badge
iris tx nft issue greendeedlevel3 --from=britt-iris-key --name=green-deeds-level-three --schema=level-three-meta.json --chain-id=green-deeds-test

````

Now Green Deeds NFTs are issued on IRISnet.  Once a user earns a badge through the Green Deeds application with their consistent regeneration efforts, and [mint](https://www.irisnet.org/docs/cli-client/nft.html#iris-tx-nft-mint) a new badge to the blockchain. 

````bash

# mint a level one badge and send to the proper recipient
iris tx nft mint greendeedlevel1 gdl1n1 --uri=image/badge-level-one.JPG --recipient=iaa1c0vhyfj3q9f3s38kccmf23vk27vmd6e9kd5jzm --from=britt-iris-key --chain-id=green-deeds-test

````

