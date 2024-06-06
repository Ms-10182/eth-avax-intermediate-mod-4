# Degen gaming tokens

This solidity code is made for tokens and redeemable feature in online Degen gaming platform. Here players can play games and buy degen tokens, then exchange that for redeemable items in the shop.

## Description
This contract is written in Solidity language, a programming language used for developing smart contracts on the Ethereum blockchain. In smart contract first we imported 3 libraries ```ERC20, Ownable, ERC@)Burnable```. In this contract player will submit request for tokens and wait in queue using ```buyDegen()``` and then the owner will mint tokens for all the players in the queue using ```mintToken()```.After receiveing tokens, player can use it to reedem cards from  enum ```Cards``` using ```redeemCards()```, or can send to other users, and if they don't need them anymore than can burn them using ```burnDegen()``` and anytime they can check their tokens through ```checkBalance()```.

# Getting Started
## Execution program

To run this code, first go to https://faucets.chain.link/ and claim free fuji testnet avax faucet using login via github. 
Now Head towards remixIDE or hardhat as per your intreset, in this project remix was used for its ease.
create a new ```MyContract.sol``` file and copy the content of ```DegenToken.sol``` into it.
In left side go to compile tab and choose the compatible compiler.
Then in deploy section choose injection wallet (metamast, phantom, etc.).
click Deploy and confirm the transaction.

### Interaction with contract
1) As player request for token in ```buyDegen()```. This will add the player to the queue.
2) Then from owner account call ```mintToken()```. This will mint token.
3) Switch to player account and check balance using ```checkBalance()```. now you can redeem cards by passing (0,1,2,3,4) for ```Cards{rare,superRare,epic,mythic,legendary}``` depending upon card rarity in exchange of tokens, or can send tokens to other player's account by calling ```transferDegen()``` or can burn the token if they don't need anymore using ```burnDegen()```.

## Authors

Mayank Sharma  
[@Mayank](https://www.linkedin.com/in/mayank-sharma-078278243/)
