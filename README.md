# Crypto

Create wallet
1. ```sh -c  "$(curl -sSfL https://release.solana.com/v1.8.5/install)"```
2. Exit out of terminal and restart terminal 
3. ```solana-keygen new```
4. Check balance for Solana ```solana balance```. Transfer Solana from the wallet of your choosing (I chose phantom), to the new wallet
5. Next, ```sudo apt update``` and run ```curl https://sh.rustup.rs -sSf | sh```. Install the file. It is the first option (Proceed with installation (default))
6. Restart terminal again
7. Run ```sudo apt install libudev-dev``` (This package contains the files needed for developing applications that use libudev)
8. Run ```sudo apt install libssl-dev pkg-config```
9. Run ```sudo apt install build-essential -y```
10. Next, install Solana token program. ```cargo install spl-token-cli```
11. Create token with ```spl-token create-token``` and copy the token ID 
12. Create an account that can hold the token. ```spl-token create-account <token id>```
13. Mint token with ```spl-token mint <token id> <amount> <account id> 
14. Check your account ```spl-token accounts```
15. Transfer it to your own wallet ```spl-token transfer --fund-recipient --allow-unfunded-recipient <token ID> <amount> <phantom wallet address> . the allow-unfunded-recipient flag means that the wallet does not have an account for our token. Allow it to be sent and we'll create one for them. 
16. Next, go to ```solscan.io``` and paste the ```token id``` into the search bar. You'll see your token on the blockchain
17. To stop minting forever, ```spl-token authorize <token id> mint --disable```
