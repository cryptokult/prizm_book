```shell
prizm_node@computer:/home/prizm-dist$ ./getStatus.sh
```

#### output 1:
```prolog
Sending blockchain status request to locally running PrizmCore

2020-10-25 00:41:21

URL:http://127.0.0.1:9976/prizm?requestType=getBlockchainStatus

[543/543] -> "response.json"

[1]

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


---
```shell
prizm_node@computer:/home/prizm-dist$ ./getStatus.sh
```

#### output 2:
```prolog
Sending blockchain status request to locally running PrizmCore

2020-10-25 00:57:58

URL:http://127.0.0.1:9976/prizm?requestType=getBlockchainStatus

[608/608] -> "response.json"

[1]

response.json content:
```
```json
{
  "apiProxy":true,  
  "correctInvalidFees":true,  
  "ledgerTrimKeep":30000,  
  "maxAPIRecords":100,  
  "blockchainState":"DOWNLOADING",  
  "currentMinRollbackHeight":43200,  
  "numberOfBlocks":44836,  
  "isTestnet":false,  
  "includeExpiredPrunable":true,  
  "isLightClient":false,  
  "services":[],  
  "requestProcessingTime":0,  
  "version":"1.10.4.4",  
  "maxRollback":800,  
  "lastBlock":"1005132562215956263",  
  "application":"PZM",  
  "isScanning":false,  
  "isDownloading":true,  
  "cumulativeDifficulty":"36167674643713",  
  "lastBlockchainFeederHeight":1236426,  
  "maxPrunableLifetime":7776000,  
  "apiProxyPeer":"82.146.55.55",  
  "time":70861199,  
  "lastBlockchainFeeder":"167.71.1.130"  
}
