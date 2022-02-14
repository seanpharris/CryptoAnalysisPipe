# CryptoAnalysisPipe

### Using CSV files as data repositories, this is the pipeline working with a RapidAPI by Alpha Vantage to call and store daily records for cryptocurrencies that I have an interest in.

### List of currencies:
| Currency code | Currency name           |
|---------------|-------------------------|
| AAVE          | Aave                    |
| ADA           | Cardano                 |
| AION          | Aion                    |
| ALGO          | Algorand                |
| AMP           | Synereo                 |
| ANC           | Anoncoin                |
| ANT           | Aragon                  |
| ARDR          | Ardor                   |
| ATM           | ATMChain                |
| ATOM          | Cosmos                  |
| AVAX          | Avalanche               |
| BAND          | Band Protocol           |
| BAT           | Basic-Attention-Token   |
| BCC           | BitConnect              |
| BCH           | Bitcoin-Cash            |
| BLZ           | Bluzelle                |
| BNB           | Binance-Coin            |
| BNT           | Bancor-Network-Token    |
| BTC           | Bitcoin                 |
| BTS           | BitShares               |
| BTT           | BitTorrent              |
| BUSD          | Binance-USD             |
| CAKE          | PancakeSwap             |
| COMP          | Compound                |
| CTXC          | Cortex                  |
| CVC           | Civic                   |
| DAI           | Dai                     |
| DAR           | Darcrus                 |
| DASH          | Dash                    |
| DATA          | DATAcoin                |
| DCR           | Decred                  |
| DENT          | Dent                    |
| DGB           | DigiByte                |
| DNT           | district0x              |
| DOGE          | DogeCoin                |
| DOT           | Polkadot                |
| EGLD          | Elrond                  |
| ELF           | aelf                    |
| ENJ           | Enjin-Coin              |
| EOS           | EOS                     |
| ETC           | Ethereum-Classic        |
| ETH           | Ethereum                |
| FIL           | Filecoin                |
| FTT           | FTX Token               |
| FUN           | FunFair                 |
| GNO           | Gnosis-Token            |
| GRT           | Graph                   |
| GTC           | Game                    |
| GTO           | Gifto                   |
| GXS           | GXShares                |
| HBAR          | Hedera                  |
| ICX           | ICON                    |
| IOST          | IOStoken                |
| IOTA          | IOTA                    |
| IOTX          | IoTeX                   |
| KLAY          | Klaytn                  |
| KMD           | Komodo                  |
| KNC           | Kyber-Network           |
| KSM           | Kusama                  |
| LEND          | EthLend                 |
| LINK          | ChainLink               |
| LRC           | Loopring                |
| LSK           | Lisk                    |
| LTC           | Litecoin                |
| LUNA          | Terra                   |
| MANA          | Decentraland            |
| MATIC         | Polygon                 |
| MCO           | Monaco                  |
| MIOTA         | IOTA                    |
| MITH          | Mithril                 |
| MKR           | Maker                   |
| MLN           | Melon                   |
| NANO          | Nano                    |
| NEO           | NEO                     |
| NMR           | Numeraire               |
| NPXS          | Pundi-X-Token           |
| NULS          | Nuls                    |
| OMG           | OmiseGo                 |
| ONT           | Ontology                |
| ORN           | Orion-Protocol          |
| POLY          | Polymath                |
| POWR          | Power-Ledger            |
| QTUM          | Qtum                    |
| SHIB          | SHIBA-INU               |
| SOL           | Solana                  |
| SNX           | Synthetix-Network-Token |
| STORJ         | Storj                   |
| STORM         | Storm                   |
| STRAT         | Stratis                 |
| STX           | Stox                    |
| SYS           | SysCoin                 |
| THETA         | Theta-Token             |
| TRIBE         | Tribe                   |
| TRX           | Tronix                  |
| TUSD          | TrueUSD                 |
| UNI           | Uniswap                 |
| UST           | TerraUSD                |
| UTK           | UTrust                  |
| VEN           | VeChain                 |
| VET           | VeChain                 |
| WAN           | Wanchain                |
| WAVES         | Waves                   |
| WTC           | Walton                  |
| XLM           | Stellar                 |
| XMR           | Monero                  |
| XRP           | Ripple                  |
| XTZ           | Tezos                   |
| XVG           | Verge                   |
| XZC           | ZCoin                   |
| ZEC           | Zcash                   |
| ZEN           | ZenCash                 |
| ZIL           | Zilliqa                 |
| ZRX           | 0x                      |

### Data features:
| Feature                                             |
|-----------------------------------------------------|
| Date                                                | 
| Opening currency value in the China market          | 
| Opening currency value in the U.S. market           | 
| Highest currency value in the China market          | 
| Highest currency value in the U.S. market           | 
| Lowest currency value in the China market           | 
| Lowest currency value in the U.S. market            | 
| Closing currency value in the China market          | 
| Closing currency value in the U.S. market           | 
| Volume                                              | 
| Market Cap: U.S. market                             | 


### The CSVs are stored into Pandas DataFrames within a dictionary.
* To access the DataFrames, use: `df_dict['<Name of Cryptocurrency>']`

- - - -

### Documentation used:
* Alpha Vantage - https://rapidapi.com/alphavantage/api/alpha-vantage/
* Documentation - https://www.alphavantage.co/documentation/
* Repo for API code  
  * https://github.com/RomelTorres/alpha_vantage
  * https://alpha-vantage.readthedocs.io/en/latest/

- - - -
  
#### Contact Info:
  * pharri.sean@gmail.com


