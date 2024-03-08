# Off-Chain NFT Allowlist

This Off-Chain NFT Allowlist is a Solidity smart contract that enables the minting of NFTs based on off-chain signatures. It allows specific addresses that are "allowlisted" to mint NFTs by providing a valid signature generated off-chain.

## Flow

1. Frontend send signing request to backend API
2. If the wallet is in allowlist, backend generate messageHash and Signature
3. Frontend call mint function using messageHash and signature
4. Using ECDSA Recover, check if the signer is same as the owner of Smart Contract
5. If YES, Mint a new NFT

## Code

Smart Contract: `/contracts/NFTAllowlist.sol`

Off-Chain Signature Generation: The signature is returned if the address is in the whitelist, see more in `/scripts/run.js`

Signature Verification

```bash
npx hardhat run scripts/run.js
```