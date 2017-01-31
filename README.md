# Coindesk's Construct 2017 Cross-Blockchain Scavenger Hunt!

## Rules and Guidelines
 - Use the Ropsten Ethereum Testnet (not the mainnet) when answering questions.
 - When answering clues, please use the same address for each clue (the one that registered the token with).
 - Please enter all clues in lowercase.
 - If you need help, ask for some tips on Slack or find some of the devs in person.
 - Any answers (not clues) that are cryptocurrency or contract addresses need to have the "0x" removed from the front of the address.
 - Contract source code is in the contracts folder and on Etherscan at their contract address.
 - Return values may not be in ASCII. You may need to convert between Hex and ASCII. You can use web3.js or an online hex to ASCII converter.

## Scavenger Hunt Steps

### Join the Hunt!
  1. Go to address [0xaA8C7310aD00Af1447747D21F2d146ecd674DebA on Etherscan](https://testnet.etherscan.io/address/0xaa8c7310ad00af1447747d21f2d146ecd674deba). The contract code is posted there, including the neccessary ABI needed to pull up the contract in Mist. Connect to Ropsten and add the contract to Mist, Browser Solidity, or any other tool that allows you to interact with smart contracts.
  If you are using Browser Solidity, you will need to:
  - Paste the contract (exactly as it appears in this repo or on Etherscan).
  - Choose the correct compiler - "soljson-v0.4.8+commit.60cc1668"
  - Connect to Ropsten using MetaMask or an RPC connection to an Ethereum client.
  - Click the green "At Address" button and enter the contract address.
  
  2. Call the joinTheHunt() function to add your Name and Shout-out message to the hunt.
  
  3. For every clue, you will need to access the smart contract and submit clues [functions are self-explanatory, getClue() and setClue()] When setting a clue, you will get get a bool true if you guess correctly or a bool false if you guess incorrectly.
  
  4. Have fun! :)

### Bitcoin Clue - Non-Standard Bitcoin Transactions, BIPS, and Riches:
Contract: [0xfb688899ad346019f053c9b0a0880b3b558d768d](https://testnet.etherscan.io/address/0xfb688899ad346019f053c9b0a0880b3b558d768d)
The questions are embedded in the smart contract :)
You can call getClue1(), getClue2(), etc... to get the 4 clues. Use setClue() to answer.

### zCash Clue - Encrypted Memo Field
Contract: [0xdcfb05a6f8bb42356e2f86893b20a345fd3ba46e](https://testnet.etherscan.io/address/0xdcfb05a6f8bb42356e2f86893b20a345fd3ba46e)

Send us a shielded transaction with a return z_address (zaddr) you control embedded in the encrypted memo field, and we'll use the memo field to send back a transaction with the clue answer to submit to the smart contract!

You'll need a running zcash daemon, a z_address, and some ZEC (0.0002 ZEC should be sufficient for one message). Anything you put in the encrypted memo field must be encoded in hexadecimal format, and must not exceed 512 bytes.

The address to send to is: zcHPJvjqbyMMiYD48QcJKmHD9Va69UwGzY3dEm5Vrqz36bCt1jA9qEtR4A2LcQnZSUqTYrEJHgEgM2NwhGfWV88H1a8V31k

1. Start up your zcash client. (Here's our guide: https://github.com/zcash/zcash/wiki/1.0-User-Guide)
2. Send a shielded transaction to the address above, with a zaddr you control embedded in the encrypted memo field. Suggested value of the transaction is 0.0001 ZEC, remember to encode your message in hex, and keep it under 512 bytes. 
	Example message: "Please send the next Construct scavenger hunt clue to zchfvC6iubfsAxaNrbM4kkGDSpwjafECjqQ1BZBFXtotXyXARz2NoYRVEyfLEKGCFRY7Xfj2Q3jFueoHHmQKb63C3zumYnU"
3. Check the zaddr you provided for an incoming transaction that will contain the next clue in its encrypted memo field. 

Tips: 
The command to get a new z_address is "./src/zcash-cli z_getnewaddress"
The command to check the balance of a zaddr is "./src/zcash-cli z_listreceivedbyaddress <your zaddr>"
Messages in the encrypted memo field are padded with 0's out to 512 bytes, so be sure to strip off the extra zeros before decoding the message you receive.
It's possible to send messages in the encrypted memo field from transparent addresses to shielded addresses, as well as shielded -> shielded. 

P.S. Here's a handy tool that can help with sending and receiving messages in the encrypted memo field: https://github.com/whyrusleeping/zmsg

## Construct Attendees Only
Once you have joined the scavenger hunt and answered both the Bitcoin and ZCash clues successfully, take a picture of yourself holding your Construct 2017 badge. Put that image on IPFS and email the IPFS hash to hudson@hudsonjameson.org. We may make a token for those who completed the scavenger hunt, so it will be like a winner list.
The first 2 people who email me with their IPFS hash after successfully completing the hunt will win an **physical ether card**. Visit [ether.card](ether.card) to learn more.

## Helpful Links

[We have a chat channel on Gitter with people willing to help. Join Souptaculatr/scavengerhunts on Gitter](https://gitter.im/Souptacular/scavengerhunts). 

https://bitcoin.stackexchange.com/

https://ethereum.stackexchange.com/

https://github.com/ipfs/ipfs

[ZCash User Help SLack](https://chat.zcashcommunity.com/channel/user-support)

## How to Get Ropsten Testnet Ether
[B9Labs Faucet](http://ipfs.b9lab.com:8080/ipfs/QmTHdYEYiJPmbkcth3mQvEQQgEamFypLhc9zapsBatQW7Y/throttled_faucet.html)

[A-Labs Faucet](http://faucet.ropsten.be:3001/)

[ether.camp Faucet](https://ropsten.ether.camp/)

[Metamask Chrome Plugin](https://metamask.io/) has a button to get free testnet ether.

## Programs to Connect to Ropsten
[Metamask](https://metamask.io/)
[For help: Metamask Slack](http://slack.metamask.io/)
[Mist](https://github.com/ethereum/mist/releases)

[geth](https://geth.ethereum.org/)

[Stack.Exchange Answer on Connecting to Ropsten from previous testnet (Morden).](https://ethereum.stackexchange.com/questions/10261/how-to-switch-from-morden-to-ropsten)
