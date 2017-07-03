# bip39-tx-signer
While there are [some tools](https://github.com/iancoleman/bip39) to easily generate your own HD-wallet using BIP39, signing a transaction on your cold storage hardware is still a hassle. I wrote this small CLI tool to make my life, and maybe yours, a bit easier.

## How-To

1. Clone this repository
2. `npm install`
3. `node index.js` for help

## Examples
To sign a transaction:

```
node index.js createEthTx --from "0xc2E87a289041fd0f04a954da6044ff8bb60927a4" --to "0xAAec6b3e1A7D9841255fAd5db80c027372496B2E" --nonce 0 --value 1 --gasPrice 21000000000 --gasLimit 21000
```

This will create a transaction for 1 ETH from `0xc2E87a289041fd0f04a954da6044ff8bb60927a4` to `0xAAec6b3e1A7D9841255fAd5db80c027372496B2E`. You will then be asked to supply your mnemonic phrase using a prompt.

**Caution** : If you use `--mnemonic` to supply your phrase, be advised that your phrase can be recovered from your bash/shell history.