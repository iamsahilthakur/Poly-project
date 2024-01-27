# NFT Collection Deployment and Polygon Bridge Transfer

Welcome to the Polygon-Advance NFT Collection Deployment project! This guide will walk you through deploying an NFT (Non-Fungible Token) collection on the Ethereum blockchain, mapping the collection to Polygon, and transferring assets via the Polygon Bridge.

## Getting Started

To get started with this project, follow these steps:

1. **Clone the Repository:**
   - Download the entire repository to access its contents.

```bash
git clone https://github.com/your-username/polygon-advance-nft
cd polygon-advance-nft
```

2. **Install Dependencies:**
   - Navigate to the main project directory.

```bash
cd path/to/polygon-advance-nft
npm install
```

3. **Run Tests:**
   - Execute the test file using the command:

```bash
npx hardhat test
```

4. **Compile the Contract:**
   - Execute the following command to compile the contract.

```bash
npx hardhat compile
```

## Deploying the ERC721 Contract

Before deploying, rename ".env" and provide your wallet private key where required (e.g., `PRIVATE_KEY='your wallet private key'`, `PUBLIC_KEY='account address'`). To deploy the ERC721 contract to the Goerli Ethereum Testnet, run the following command:

```bash
npx hardhat run scripts/deploy.js --network goerli
```

**Note:** After deploying, the contract address will be generated. Copy the address into "contarctAddress.js" (stored in the metadata folder) and "batchMint.js" (stored in the scripts folder).

## Batch Mint NFTs

To batch-mint NFTs using the deployed ERC721 contract, run the following command:

```bash
npx hardhat run scripts/mint-nft.js --network goerli
```

The script will mint the specified number of NFTs and assign them to your address.

## Approve and Deposit NFTs to Polygon Mumbai

To approve and deposit the minted NFTs from Ethereum to the Polygon Mumbai network using the FxPortal Bridge, execute the following commands:

```bash
npx hardhat run scripts/batchTransfer.js --network goerli
```

## Author

This project is authored by Sahil.

## License

This project is licensed under the MIT License. 
