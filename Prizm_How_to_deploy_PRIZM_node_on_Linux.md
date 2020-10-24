### How to deploy PRIZM node on Linux

#### Requirements to equipment

>OS Linux (Ubuntu)  
CPU 2 and more
RAM 2GB and more  
Free disk space 64GB and more

---
#### 1st step - Get soft on your machine
The [Prizm Core Wallet](https://github.com/cryptokult/prizm_core_wallet) is located in written in Java, so we need first to install the [JRE™- Java Runtime Environment](https://www.oracle.com/java/technologies/javase-jre8-downloads.html).

##### 1. Prism Core Setup
You can get the Prizm Core Wallet from [prizm-dist](http://tech.prizm.space/files/prizm-dist-1.10.4.4-linux.tgz) archive.

Download
```shell
```

Navigate
```shell
$ cd "~/Downloads"
```

Move the `.tar.gz` archive binary to the current directory
```shell
```
Unpack the prizm-dist archive file:
```shell
$ tar zxvf \
           prizm-dist-1.10.4.4-linux.tgz
```
[output log file for 1.10.4.2](./logs/prizm-dist-1.10.4.2-linux.tgz_setup_console_log.md)  
[output log file for 1.10.4.4](./logs/prizm-dist-1.10.4.4-linux.tgz_setup_console_log.md)

```prolog
WARNING: Peers.<clinit>: Your announced address is not valid: java.net.UnknownHostException: PRIZM-XXXX-XXXX-XXXX-XXXX: Temporary failure in name resolution
```

Delete `prizm-dist` archive file
```shell
$rm ./prizm-dist-1.10.4.4-linux.tgz
```

##### 2. JRE™ Setup

[Download JRE™](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)

Download `Linux x64 Compressed Archive` `jre-8u271-linux-x64.tar.gz`
```
https://download.oracle.com/otn/java/jdk/8u271-b09/61ae65e088624f5aaa0b1d2d801acb16/jre-8u271-linux-x64.tar.gz?AuthParam=1603466208_0f9aa41a66068cf28e637640b75758d8
```

Extract the `JRE™` tar.gz archive in `prizm-dist` folder:
```shell
$ cd "~/Downloads/prizm-dist"
```

Unpack the `JRE™` archive file:
```shell
$ tar zxvf \
           jre-8u271-linux-x64.tar.gz
```
[output log file](./logs/jre-8u271-linux-x64.tar.gz_setup_console_log.md)

Delete `JRE™` archive file
```shell
$rm ./jre-8u271-linux-x64.tar.gz
```


##### Results:
```prolog
/home/
|— prizm-dist/
| |— conf/
| |— jre/
| | |— [jre files]
| |— prizm_db/
| |— html/
| |— logs/
| |— run.sh
| |— run_test.sh
| |— prizmEngine.jar
```

---
#### 2nd step - Setup your wallet address

Yep!), we unpacked `prizm-dist` and `jre`.

In this step we need to adjust `prizm.default.properties`:

1. We open `conf/prizm.default.properties`
2. Move to line 61 `(myAddress=)`` and insert your address.
3. Move to line 250 `(prizm.adminPassword)` and insert your password.
4. Save `prizm.default.properties`

---
#### 3rd step
Testing and running prizmEngine:

1. Run the `run-test.sh` and see if there are any errors?  
[output log file](./logs/prizm_dist_run_test.sh_console_log_for_1.10.4.4_fixed-conf.md)  

2. I hope that number of errors is 0 and we move to next step.

3. Open the browser and input: `ip:9976`

**Where ip: IP = prizm.myAddress.**

http://localhost:9976/index.html

##### ctrl-C
[output log file for 1.10.4.2](./prizm_dist_run_test.sh_ctrl-c_console_log_for_1.10.4.2.md)

if you see index.html file and stable connection then all is well.

Kill java process:

- First command:
```shell
$ ps -A | grep java
```
- Output of this command will give the list of java processes running on your system. Note down Process ID (PID) `prizmEngine.jar`.
- Second command:
```shell
$ kill -9 PID
```
- Wait 3 minutes while databases `prizmEngine` are closed.
- Start `run.sh` and be connected to the `ip:9976`  
[output log file](./logs/prizm_dist_run.sh_console_log.md)

Get Info status about Prizm Node
```shell
$ getStatus.sh
```
[output log file](./logs/prizm_dist_getStatus.sh_console_log.md)
