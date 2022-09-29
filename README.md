# try-sui

Try sui > https://docs.sui.io/

My random notes on sui.

---

1. Install Sui Wallet - https://docs.sui.io/devnet/explore/wallet-browser
2. Mint NFTs in Sui Wallet
3. Register Sui name - https://sui-names.com/
4. Sui Explorer - https://explorer.devnet.sui.io/
5. Install Sui - https://docs.sui.io/devnet/build/install
6. Request faucet in Discord - https://discord.com/channels/916379725201563759/971488439931392130
7. Connect to Sui Devnet

### Install Sui

```
cargo install --locked --git https://github.com/MystenLabs/sui.git --branch "devnet" sui sui-gateway
```

I found an issue with :

```
    Updating git repository `https://github.com/MystenLabs/sui.git`
error: could not find `sui` in https://github.com/MystenLabs/sui.git with version `*`
    Updating git repository `https://github.com/MystenLabs/sui.git`
error: could not find `sui-gateway` in https://github.com/MystenLabs/sui.git with version `*`
     Summary Failed to install sui, sui-gateway (see error(s) above).
error: some crates failed to install
```

so I try to update cargo and rust to latest version:

```
rustup update stable
```

and then reinstall again, it should works, waiting for compiling and installing... 

```
sui --version
```

```
sui 0.10.0
```

## Start Sui Client

> Reference : https://docs.sui.io/devnet/build/devnet

```
sui client

# config file located in ~/.sui/sui_config/client.yaml
```

Follow the prompt to continue.

Save your keypair (address) and **Secret Recovery Phrase**

Switch Sui client to devnet gateway

```
sui client switch --rpc https://gateway.devnet.sui.io:443
```

Request faucet at #devnet-faucet on Discord

```
!faucet <YOUR_ADDRESS>
```

Check your current address by:

```
sui client active-address
```

Create example NFT

```
sui client create-example-nft
```

Customize info:

```
sui client create-example-nft --url=https://devahoy.com/static/images/avatar.png --description
="This is Chai" --name="Chai"
```

I'm here 🤣 - https://explorer.devnet.sui.io/objects/0xd130873da3cfbd99f31489c1a675230e0af95166

## Discover explorer

## Smart Contract
