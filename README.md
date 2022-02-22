# CryptoAnalysisPipe
- - - -
## About
* This is a pipeline that keeps cryptocurrency data up to date
* The data comes from a RapidAPI by Alpha Vantage to call and store daily records for cryptocurrencies
* Each crypto's data is stored its own CSV file (files found in kaggle)
* It updates the data every Wednesday at midnight 
* The notebook can be found at [here](https://www.kaggle.com/seanpharris/cryptoanalysispipe)
* You may run the notebook yourself or use the output files from the one I made (linked above)
- - - - 
## Intentions
My hopes are to be able to do data analysis with fresh data of the currencies and allow others to access the output files of the notebook
- - - -
## Table of Contents
1. [Requirements](#requirements)
2. [Pipe Process](#pipe-process)
3. [Data features](#data-features)
4. [Use](#use)
5. [List of currencies](#list-of-currencies)
6. [Documentation used](#documentation-used)
7. [Contact Info](#contact-Info)
- - - -
### Requirements
To run this on your own you will have to sign up for an account at [RapidAPI](https://rapidapi.com/alphavantage/api/alpha-vantage/) to get a RapidAPI Key
In the notebook, there is a variable called "API_KEY". This is where you will use your key.
To make your key a secret on Kaggle:
1. Navigate to the top of the notebook in Edit
2. click "Add-Ons" 
3. click "Secrets"
4. click "Add a new secret" 
5. In the "Label" text field - type "API_KEY"
6. In the "Value" text field - copy and paste your API key from RapidAPI
7. Click "Save"
8. Below "Save" click "Copy-clipboard"
9. Click "Done"
10. Paste into a new cell towards the top of your notebook  
It should looks something like:  

from kaggle_secrets import UserSecretsClient  
user_secrets = UserSecretsClient()  
secret_value_0 = user_secrets.get_secret("API_KEY")  

- - - - 
### Pipe Process
* The input file "currency-list.csv" is used to put together the DataFrame dictionary
* The name of each currency is then associated with its most recent CSV file in the dictionary
* The date for today is found and is compared to the last updated date; that range is then put into a list
* Each currencies DataFrame is updated with the data for that date range
* Once the DataFrame is updated - it writes to the associated CSV
* In the notebook, you can find examples of the DataFrame dictionary 

If you choose to run it on your own - beware: it takes a while because you can only make up to 5 calls per a minute

- - - -
### Data features
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
- - - -
### Use
The CSVs are stored into Pandas DataFrames within a dictionary.
* To access the DataFrames, use: `df_dict['<Currency name>']`
- - - -
### List of currencies
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
- - - -

### Documentation used
* Alpha Vantage - https://rapidapi.com/alphavantage/api/alpha-vantage/
* Documentation - https://www.alphavantage.co/documentation/
* Repo for API code  
  * https://github.com/RomelTorres/alpha_vantage
  * https://alpha-vantage.readthedocs.io/en/latest/

- - - -
  
### Contact Info
  * pharri.sean@gmail.com


