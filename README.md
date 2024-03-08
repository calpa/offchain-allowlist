# Off-Chain NFT Allowlist

This Off-Chain NFT Allowlist is a Solidity smart contract that enables the minting of NFTs based on off-chain signatures. It allows specific addresses that are "allowlisted" to mint NFTs by providing a valid signature generated off-chain.

## How it Works

Smart Contract: `/contracts/NFTAllowlist.sol`

Off-Chain Signature Generation: The signature is returned if the address is in the whitelist, see more in `/scripts/run.js`

Signature Verification

```bash
npx hardhat run scripts/run.js
```