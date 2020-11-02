```shell
prizm_node@computer:/home/prizm-dist$ ./run_test.sh 
```
output:
```prolog
Initializing Prizm server version 1.10.4.4
Command line arguments
-Xms1g
-Xmx3g
isHeadless=false
Runtime mode prizm.env.CommandLineMode
User home folder /home/prizm-dist
Loading prizm.default.properties from classpath
Loading logging-default.properties from classpath
2020-10-25 00:30:38 INFO: prizm.enableStackTraces = "true"
2020-10-25 00:30:38 INFO: prizm.enableLogTraceback = "true"
2020-10-25 00:30:38 INFO: Logger.<clinit>: logging enabled
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: socksProxyHost not defined
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: socksProxyPort not defined
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.isTestnet = "false"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.isOffline = "false"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.isLightClient = "false"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.customLoginWarning not defined
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.maxRollback = "800"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.trimFrequency = "1000"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.batchCommitSize not defined or not numeric, using default value 100
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.maxPrunableLifetime = "7776000"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.includeExpiredPrunable = "true"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.measureTrimmingTime = "false"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.correctInvalidFees = "true"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.maxBlockchainHeight not defined or not numeric, using default value 0
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.serveOnlyLatestTransactions not defined, using default false
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbParaUsername = "sa"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbParaPassword = "para"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.statementLogThreshold = "10000"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.transactionLogThreshold = "15000"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.transactionLogInterval = "15"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.dbCacheKB = "0"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbUrl not defined
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbType = "h2"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbDir = "./prizm_db/prizm"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbParams = "DB_CLOSE_ON_EXIT=FALSE;MVCC=TRUE;MV_STORE=FALSE"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbUsername = "sa"
2020-10-25 00:30:38 INFO: Prizm.getStringProperty: prizm.dbPassword = "{not logged}"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.maxDbConnections = "30"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.dbLoginTimeout = "70"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.dbDefaultLockTimeout = "60"
2020-10-25 00:30:38 INFO: Prizm.getIntProperty: prizm.dbMaxMemoryRows = "1000000"
2020-10-25 00:30:38 INFO: Prizm.getBooleanProperty: prizm.useStrongSecureRandom not defined, using default false
2020-10-25 00:30:39 INFO: DbVersion.init: Database update may take a while if needed, current db version 496...
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableTransactionRebroadcasting = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.testUnconfirmedTransactions not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxUnconfirmedTransactions = "2000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.trimDerivedTables = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.numberOfForkConfirmations = "1"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.simulateEndlessDownload not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableGetMoreBlocksThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableProcessTransactionsThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableRebroadcastTransactionsThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableRemoveUnconfirmedTransactionsThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableProcessWaitingTransactionsThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enablePublicKeyCache = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.ledgerTrimKeep = "30000"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.ledgerAccounts = "*"
2020-10-25 00:30:39 INFO: AccountLedger.<clinit>: Account ledger is tracking all accounts
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.ledgerLogUnconfirmed = "2"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.hideErrorDetails = "false"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.myPlatform = "Unknown"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.myAddress = "93.178.105.7"
2020-10-25 00:30:39 INFO: UPnP.init: Looking for UPnP gateway device...
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.upnpGatewayTimeout not defined or not numeric, using default value 7000
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.upnpDiscoverTimeout not defined or not numeric, using default value 3000
2020-10-25 00:30:39 INFO: UPnP.init: External IP address is 93.178.105.7
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.peerServerPort = "9974"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.shareMyAddress = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enablePeerUPnP = "false"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.myHallmark not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.adminPassword = "{not logged}"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxAPIRecords = "100"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableAPIUPnP = "false"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.apiServerIdleTimeout = "30000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.apiServerCORS = "true"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.forwardedForHeader not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.disabledAPIs not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.disabledAPITags not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.allowedBotHosts = "*"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableAPIServer = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.apiServerPort = "9976"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.apiServerSSLPort = "9976"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.apiServerHost = "127.0.0.1"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableAdminPassword = "false"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.keyStoreType not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.keyStorePassword = "{not logged}"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.apiSSL = "false"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.apiServerEnforceSSL = "true"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.keyStorePath = "keystore"
2020-10-25 00:30:39 INFO: API.<clinit>: API server using HTTP port 9976
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.apiResourceBase = "./html/ui"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.apiWelcomeFile = "index.html"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.javadocResourceBase = "./html/doc"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableAPIServerGZIPFilter = "false"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.apiFrameOptionsSameOrigin = "true"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.defaultPeers = "94.130.167.167; 188.40.185.117; 138.201.196.91; 148.251.142.180; 138.201.196.91; 88.99.219.100; 144.91.94.78; 176.9.112.235; 193.109.79.183; 95.31.104.238; 195.93.180.128; 176.223.130.3; 62.109.24.251; 185.246.65.68; 91.240.87.54; 45.143.137.203; 91.234.34.249; 167.71.1.130; 62.109.27.72; 185.56.138.188; 212.224.113.19;"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.wellKnownPeers = "94.130.167.167; 188.40.185.117; 138.201.196.91; 148.251.142.180; 138.201.196.91; 88.99.219.100; 144.91.94.78; 176.9.112.235; 193.109.79.183; 95.31.104.238; 195.93.180.128; 176.223.130.3; 62.109.24.251; 185.246.65.68; 91.240.87.54; 45.143.137.203; 91.234.34.249; 167.71.1.130; 62.109.27.72; 185.56.138.188; 212.224.113.19;"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.knownBlacklistedPeers not defined
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxNumberOfInboundConnections = "1000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxNumberOfOutboundConnections = "100"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxNumberOfConnectedPublicPeers = "40"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxNumberOfKnownPeers = "2000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.minNumberOfKnownPeers = "1000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.connectTimeout = "1000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.readTimeout = "2000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableHallmarkProtection = "false"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.pushThreshold = "500000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.pullThreshold = "500000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.useWebSockets = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.webSocketIdleTimeout = "90000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enablePeerServerGZIPFilter = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.blacklistingPeriod = "6000000"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.communicationLoggingMask = "0"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.sendToPeersLimit = "10"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.usePeersDb = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.savePeers = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.getMorePeers = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.cjdnsOnly = "false"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.ignorePeerAnnouncedAddress = "false"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disablePeerConnectingThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disablePeerUnBlacklistingThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableGetMorePeersThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.peerServerHost = "0.0.0.0"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.peerServerIdleTimeout = "3000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enablePeerServerDoSFilter = "true"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.peerServerDoSFilter.maxRequestsPerSec = "30"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.peerServerDoSFilter.delayMs = "1000"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.peerServerDoSFilter.maxRequestMs = "300000"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableAPIProxy = "true"
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.apiProxyBlacklistingPeriod = "1800000"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.forceAPIProxyServerURL not defined
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.allowAPIHierarchyWithoutPassword = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.allowAPIHierarchyOnlyLocalhost = "true"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableAPIProxyPeersUpdateThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getIntProperty: prizm.maxNumberOfForgers = "100"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableFakeForging not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.disableGenerateBlocksThread not defined, using default false
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.addOns not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.allowedUserHosts = "127.0.0.1; localhost; [0:0:0:0:0:0:0:1];"
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.enableUIServer = "false"
2020-10-25 00:30:39 INFO: Users.<clinit>: User interface server not enabled
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.debugTraceQuote = """
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.debugTraceSeparator = "        "
2020-10-25 00:30:39 INFO: Prizm.getBooleanProperty: prizm.debugLogUnconfirmed = "true"
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.debugTraceAccounts not defined
2020-10-25 00:30:39 INFO: Prizm.getStringProperty: prizm.debugTraceLog not defined
2020-10-25 00:30:41 INFO: ParaEngine.log: 0 - Using new rollback algorithm as default from Genesis block
2020-10-25 00:30:41 INFO: ParaEngine.log: DATABASE INITIALIZED
2020-10-25 00:30:41 INFO: BlockchainProcessorImpl.addGenesisBlock: Genesis block already in database
2020-10-25 00:30:41 INFO: BlockchainProcessorImpl.addGenesisBlock: Last block height: 0
2020-10-25 00:30:41 INFO: Prizm.getBooleanProperty: prizm.forceScan = "false"
2020-10-25 00:30:41 INFO: Prizm.getBooleanProperty: prizm.apiServerEnforcePOST = "true"
2020-10-25 00:30:41 INFO: Peers$Init.lambda$static$0: Started peer networking server at 0.0.0.0:9974
2020-10-25 00:30:41 INFO: API.lambda$static$1: Started API server at 127.0.0.1:9976
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Initialization took 3 seconds
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Prizm server 1.10.4.4 started successfully.
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Copyright © 2013-2016 The Nxt Core Developers.
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Copyright © 2016-2017 Jelurida IP B.V.
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Distributed under the Jelurida Public License version 1.0 for the N.x.t Public Blockchain Platform, with ABSOLUTELY NO WARRANTY.
2020-10-25 00:30:42 INFO: Prizm$Init.<clinit>: Client UI is at http://localhost:9976/index.html
```
