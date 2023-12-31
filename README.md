# NFT Compression 

This repository provides examples of how to mint and interact with compressed NFTs.

## Scripts

### E2E

Runs a compression example end-to-end. Mints a collection NFT and a compressed NFT for that collection, and then transfers it to another wallet. The transfer calls the Helius compression indexer to verify ownership before transferring and to include the current proof in the transfer txn.


```
npm run e2e
```

### BURN

Provided the assetId of a compressd nft owned by the wallet passed in SECRET_KEY, this script proceeds to burn it.

```
npm run burn -- --assetId=<base58 encoded assetId>
```

### REDEEM

Provided the assetId of a compressd nft owned by the wallet passed in SECRET_KEY, this script redeems an NFT (remove from tree and store in a voucher PDA).

```
npm run redeem -- --assetId=<base58 encoded assetId>
```

### CANCEL REDEEM

Provided the assetId of a compressd nft owned by the wallet passed in SECRET_KEY, this script cancels the redemption of an NFT (Put the NFT back into the Merkle tree).

```
npm run cancel-redeem -- --assetId=<base58 encoded assetId>
```
