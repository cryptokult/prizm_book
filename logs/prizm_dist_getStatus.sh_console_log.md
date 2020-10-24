```shell
prizm_node@computer:/home/prizm-dist$ ./getStatus.sh
```
```prolog
Sending blockchain status request to locally running PrizmCore


2020-10-25 00:41:21

URL:http://127.0.0.1:9976/prizm?requestType=getBlockchainStatus

[543/543] -> "response.json" [1]


response.json content:
```
```json
{
  "apiProxy":false,  
  "correctInvalidFees":true,  
  "ledgerTrimKeep":30000,  
  "maxAPIRecords":100,  
  "blockchainState":"DOWNLOADING",  
  "currentMinRollbackHeight":0,  
  "numberOfBlocks":1,  
  "isTestnet":false,  
  "includeExpiredPrunable":true,  
  "isLightClient":false,  
  "services":[],  
  "requestProcessingTime":1,  
  "version":"1.10.4.4",  
  "maxRollback":800,  
  "lastBlock":"7024118705028086222",  
  "application":"PZM",  
  "isScanning":false,  
  "isDownloading":false,  
  "cumulativeDifficulty":"0",  
  "lastBlockchainFeederHeight":0,  
  "maxPrunableLifetime":7776000,  
  "time":70860201,
  "lastBlockchainFeeder":null
}

```
