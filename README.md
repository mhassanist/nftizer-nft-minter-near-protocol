# NFTizer | NFT Minter on NEAR Protocol

## Smart Contract Sample Usage

### Build
```
env 'RUSTFLAGS=-C link-arg=-s' cargo build --target wasm32-unknown-unknown --release
```

### Deploy 
```
$ near deploy --wasmFile target/wasm32-unknown-unknown/release/near_spring_nft.wasm --accountId nftizer.mhassanist.testnet 
```

### Intialize the contract (call one time only)
```
$ near call nftizer.mhassanist.testnet  new_default_meta '{"owner_id": "'mhassanist.testnet'"}' --accountId mhassanist.testnet
```

### Minting
```
near call nftizer.mhassanist.testnet nft_mint '{"token_id": "Yom3", "receiver_id": "'msaudi.testnet'", "token_metadata": { "title": "KidPhotos3", "description": "Beautiful Kids NFTs", "media": "https://bafybeiab33alpecxhqr4bciie7jfgwcgbc7yj27utdrcfa7uzx46mjff5q.ipfs.nftstorage.link/", "copies": 1}}' --accountId mhassanist.testnet --deposit 0.1
```
