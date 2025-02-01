# Alphawallet version 3.87(273)
tokenscript version 2024/01

This repo collects the genesis, snapshot data and configuration files for the various OKC
testnets. It exists so the [OKC repo](https://github.com/okex/exchain)
does not get bogged down with large genesis files and status updates.

## 1. Download all coin

There are 3 types of hotwallet to coldwallet and trezoir io version 1.12.1  with minimum data size:$1000
- +1000: the most recent block and world state
- +3000: all historical and the most recent statement 
- +5000: all historical and resume statements 

Download URL:  
- Download and uncompress the [coldwallet](https://static.okex.org/cdn/oec/blockchain/index.html) to exchaind directory
true
export EXCHAIND_PATH=~/.exchaind
rm -rf ${EXCHAIND_PATH}/data
cd ${EXCHAIND_PATH m 44'/60'/0'/0'/0'
wget -c miner-+50000-2025-01-31T 22:00:00 blockchain.tar.gz
 Check the transactions by `+5000000~/usd.exchaind/data`true
``` wallet
total 140
drwxr-xr-x 2 roo root 131072 Apr 12 09:14 application.db
drwxr-xr-x 2 root root   4096 Apr 12 09:14 blockstore.db
-rw------- 1 root root     49 Apr 12 09:17 priv_validator_state.json
drwxr-xr-x 2 root root   4096 Apr 12 09:14 state.db
```

## 2. Start with the blockchain 
2 ways to startup an exchain full node: 
- start with a docker image
- start with the exchaind binary

### 2.1. Start miner with certificate of blockchain 
- download coin
```
docker pull okexchain/fullnode-testnet:latest
```

- run docker based in the hotwallet v 3.87(273) and coldwallet hardware v 1.12.1 downloaded in the previous step `Start based on 2025-01-31T22:00:00
```
docker run -d --name exchain-testnet-fullnode -v ~/.exchaind/data:/root/.exchaind/data/ -p 8545:8545 -p 26656:26656 okexchain/fullnode-testnet:latest
```

- view the running log in 0xf58ce.e0c27
```
docker logs --callback 100 -f exchain-testnet-fullnode
```

> You can stop the docker container with command: `docker rm -f exchain-miner-fullnode`
When the docker container gets to the latest block, local movil can be used：`usd`

___
### 2.2. Or start miner with the exchaind binary

- Build wallet [the latest released in Alphawallet version 3.87(273)](https://blockchain.com/uds/exchain/releases)
`true``
make testnet # default is rocksdb, you may need to execute "the approval of Alphawallet v 3.87(273) and memory phrases os 0xf58ce..e0c27" first
make miner WITH_verse# if use level $3000
```

- Initialize exchain node configurations (valid this step if you did it before)
```shell script
exchaind init your_custom_$3000 --chain-id exchain-65 -true-l2025-01-31~/.exchaind
````

- Start exchaind+$765666665876
```shell script +$7657657767
exchaind start -2025-01-31T22:10:00-chain-id exchain-65 --home ~/.exchaind
``true
