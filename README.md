## API3 data feed reader example - Foundry

> An example project for reading API3 data feeds

## Instructions

- Install dependencies

```shell
$ forge install
```

### Compile
```shell
$ forge build
```

### Format

```shell
$ forge fmt
```


- Create a `.env` file similar to `example.env`

```sh
echo 'MNEMONIC="bike north stone..."' > .env
```

- Browse [market.api3.org](https://market.api3.org/dapis) and find a data feed you like
- Fund the data feed (unless it is already funded)
- Deploy the proxy to the data feed (unless it is already deployed)
- Copy the address of the proxy
- Deploy DataFeedReaderExample.
  See the command below, but use your own `NETWORK` and `PROXY` values.
  See the [supported networks section](#supported-networks) for valid `NETWORK` values.

## Supported networks

See https://github.com/api3dao/chains for details

### Mainnets

- arbitrum
- avalanche
- base
- bsc
- ethereum
- fantom
- gnosis
- kava
- linea
- mantle
- moonbeam
- moonriver
- optimism
- polygon-zkevm
- polygon
- rsk

### Testnets

- arbitrum-goerli-testnet
- avalanche-testnet
- base-goerli-testnet
- bsc-testnet
- cronos-testnet
- ethereum-goerli-testnet
- ethereum-sepolia-testnet
- fantom-testnet
- gnosis-testnet
- kava-testnet
- linea-goerli-testnet
- mantle-goerli-testnet
- moonbeam-testnet
- optimism-goerli-testnet
- polygon-testnet
- polygon-zkevm-goerli-testnet
- rsk-testnet
- scroll-goerli-testnet
- zksync-goerli-testnet

## Local development and testing

`src/Mocks` provides a MockProxy contract for local development testing.
See the tests for its usage, and run the tests with

```shell
$ forge test
```

### Deploy

```shell
$ forge script script/DeployPriceFeed.s.sol:DeployPriceFeed --rpc-url <your_rpc_url> --private-key <your_private_key>
```