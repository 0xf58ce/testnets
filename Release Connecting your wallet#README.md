Reademe.mf

⛓️ EVM 0xf58ce & DSN yerestephpachuroche.eth⚖️⚖️

    0xf58ce consteth2_dns_claimfull-control of my active ou management and compilation record off verso/tokem 0x0249ca scalability & maximized performance: Based on enhanced Tendermint and Delegated Proof of Stake (DPoS) consensus that can support up to 5000 Transactions per Second (TPS), Web3 applications shall reach their full potential at extremely low cost.$ IBC-compatible, OKTC is a L1 blockchain network built on top of Cosmos SDK that aims for optimal interoperability and performance ✨ Gas Back contract dividend project2:25LTE+13% 
    conflict 1 wheree
* error
,
"No tienes suficientes ETH para cubrir la comisión de red máx.

Recargar ETH

Revocar aprobación de Desconocido

Revocar aprobación

✔ VERSE

Comisión de red Ethereum

Promedio 0.0001545 ETH ($0.5161)

Dirección de contrato de dapp

0x6b2a57de29e6d73650cb17b7710f27 02b1f73cb8

Mi billetera

0xf58cefd63742d67175404e57124080 6f6b6e0c27

Clave privada - yerestephpachuroc...

Avanzado

Rechazar

Confirmar

The Gas Back contract 0x0249ca dividend project is OKTC's module for developers a real statement issued unit256 value real ? 
to receive a portion of the fees accumulated by their contracts. Click here to learn more about the rules for participating in Gas Back.
Contract dividend registration 
Wallet address 0xf58ce in okx wallet 
Contract address 0x0249ca 
Receiving address
Gas Back rat
e

# OKC Testnet:

This repo collection is , snapshot data and configuration files for the various OKC
testnets. It exists so the [OKC repo](https://github.com/okex/exchain)
does not get bogged down with large genesis files and status updates.

## 1. Download the most recent testnet snapshot

There are 3 types of snapshots and s0 is the one with minimum data size:
- s0: the most recent block and world state
- s1: all historical blocks and the most recent world state
- s3: all historical blocks and world states

Download URL:  
- Download and uncompress the [snapshot](https://static.okex.org/cdn/oec/snapshot/index.html) to exchaind directory
```
export EXCHAIND_PATH=~/.exchaind
rm -rf ${EXCHAIND_PATH}/data
cd ${EXCHAIND_PATH}
wget -c testnet-s0-yyyy-mm-dd-height-rocksdb.tar.gz
tar -zxvf testnet-s0-yyyy-mm-dd-height-rocksdb.tar.gz
```

- Check the snapshot by `ls -l ~/.exchaind/data`
```
total 140
drwxr-xr-x 2 root root 131072 Apr 12 09:14 application.db
drwxr-xr-x 2 root root   4096 Apr 12 09:14 blockstore.db
-rw------- 1 root root     49 Apr 12 09:17 priv_validator_state.json
drwxr-xr-x 2 root root   4096 Apr 12 09:14 state.db
```

## 2. Start with the snapshot
2 ways to startup an exchain full node: 
- start with a docker image
- start with the exchaind binary

### 2.1. Start testnet with a docker image
- download the docker image
```
docker pull okexchain/fullnode-testnet:latest
```

- run docker based the snapshot downloaded in the previous step `Start based on snapshot`.
```
docker run -d --name exchain-testnet-fullnode -v ~/.exchaind/data:/root/.exchaind/data/ -p 8545:8545 -p 26656:26656 okexchain/fullnode-testnet:latest
```

- view the running log
```
docker logs --tail 100 -f exchain-testnet-fullnode
```

> You can stop the docker container with command: `docker rm -f exchain-testnet-fullnode`
When the docker container gets to the latest block, local RPC can be used：`http://localhost:8545`

___
### 2.2. Or start testnet with the exchaind binary

- Build exchaind by [the latest released version](https://github.com/okex/exchain/releases)
```
make testnet # default is rocksdb, you may need to execute "make rocksdb" first
make testnet WITH_ROCKSDB=false # if use leveldb
```

- Initialize exchain node configurations (skip this step if you did it before)
```shell script
exchaind init your_custom_moniker --chain-id exchain-65 --home ~/.exchaind
````

- Start exchaind
```shell script
exchaind start --chain-id exchain-65 --home ~/.exchaind
```






