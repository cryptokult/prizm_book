### How to deploy PRIZM node on Linux

#### Requirements to equipment

OS Linux (Ubuntu)

CPU 2 and more

RAM 2GB and more

Free disk space 64GB and more

---
#### 1st step
Now, we install prizm-dist and jre.

The Prizm core is written in Java, so we need jre under Linux:

Download jre (https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)
Download prizm-dist (http://tech.prizm.space/files/prizm-dist-1.10.4.2-linux.tgz)
Extract a prizm-dist-1.10.4.2-linux.tgz:
Change to the directory «home»:
cd /home/
Move the .tar.gz archive binary to the current directory.
Unpack the tarball:
tar zxvf prizm-dist-1.10.4.2-linux.tgz
Delete prizm-dist-1.10.4.2-linux.tgz
Extract a jre in prizm-dist folder:
Move jre tar.gz to /home/prizm-dist/
Let's now extract the zip file into that folder:
tar zxvf jre-8u202-linux-x64.tar.gz

Delete jre-8u202-linux-x64.tar.gz

Results:
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
#### 2nd step

Yep!), we installed prizm-dist and jre.

And so, the following step we will adjust prizm.default.properties:

1. We open conf/prizm.default.properties
2. Move to line 61 (myAddress=) and insert your address.
3. Move to line 250 (prizm.adminPassword) and insert your password.
4. Save prizm.default.properties

---
#### 3rd step
Testing and running prizmEngine:

1. Run the run-test.sh and see if there are any errors?
2. I hope that number of errors is 0 and we move to next step.
3. Open the browser and input: ip:9976

**Where ip: IP = prizm.myAddress.**

if you see index.html file and stable connection then all is well.

Kill java process:
- First command: ps -A | grep java
- Output of this command will give the list of java processes running on your system. Note down Process ID (PID) prizmEngine.jar.
- Second command: kill -9 PID
- Wait 3 minutes while databases prizmEngine are closed.
- Start run.sh and be connected to the ip:9976
