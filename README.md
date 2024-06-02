## This JavaScript project allows you to mint NFTs with specific metadata and manage them. The metadata includes the country, currency, continent, and population. 
## The project provides functions to mint new NFTs, list all minted NFTs, and get the total number of NFTs minted.

## Features

  Minting NFTs: Create new NFTs with specified metadata.
  Listing NFTs: Display metadata of all minted NFTs.
  Total Supply: Get the total number of NFTs minted.

## Usage

### 1. Create a variable to hold your NFTs

```javascript
const NFTs = [];
```

This line creates an empty array called `NFTs` to store all the NFT objects.

### 2. Minting an NFT

```javascript
function mintNFT(country, currency, continent, population) {
    const nft = {                
        country: country,
        currency: currency,
        continent: continent,
        population: population
    };
    NFTs.push(nft);
    console.log("Minted: " + country);
}
```

- **Parameters**:
  - `country` (string): The name of the country.
  - `currency` (string): The currency used in the country.
  - `continent` (string): The continent where the country is located.
  - `population` (string): The population of the country.

### 3. Listing all NFTs

```javascript
function listNFTs() {
    for (let i = 0; i < NFTs.length; i++) {
        console.log("\nID \t\t  :" + (i + 1));
        console.log("Country   :" + NFTs[i].country);
        console.log("Currency  :" + NFTs[i].currency);
        console.log("Continent :" + NFTs[i].continent);
        console.log("Population:" + NFTs[i].population);
    }
}
```

This function prints the metadata of all minted NFTs to the console.

### 4. Getting the total supply of NFTs

```javascript
function getTotalSupply() {
    return NFTs.length;
}
```

This function returns the total number of NFTs minted.

## Example

```javascript
// Minting NFTs
mintNFT("India", "INR", "Asia", "1.4 billion");
mintNFT("USA", "USD", "North America", "331 million");
mintNFT("Germany", "EUR", "Europe", "83 million");
mintNFT("Brazil", "BRL", "South America", "213 million");

// Listing all NFTs
listNFTs();

// Getting the total supply of NFTs
console.log("\nTotal NFTs minted: " + getTotalSupply());
```

### Expected Output

```
Minted: India
Minted: USA
Minted: Germany
Minted: Brazil

ID        :1
Country   :India
Currency  :INR
Continent :Asia
Population:1.4 billion

ID        :2
Country   :USA
Currency  :USD
Continent :North America
Population:331 million

ID        :3
Country   :Germany
Currency  :EUR
Continent :Europe
Population:83 million

ID        :4
Country   :Brazil
Currency  :BRL
Continent :South America
Population:213 million

Total NFTs minted: 4
```
