# UDPN BN-Service

## What is BN-Service?
The end users interact with the UDPN through Business Nodes owned and set up by third-party businesses who wish to integrate UDPN services to their business systems. All Business Node owners must undergo a strict KYC check before connecting to the UDPN. Like the Validator Nodes, the code for the Business Nodes is open source, and any software engineer can download the code and install it on their company’s  systems locally. 

<div align="center">
<img src=./bn.png />
</div>

To install a Business Node, businesses need to submit an application. Once approved by the Validator Node’s governance system, the Business Node is added to the UDPN and connected to the business IT system. A certificate and a DID can be created for a Business Node after the Validator Nodes’ approval. 

Each Business Node contains a gateway and private storage (encrypted by a Business Node private key). Business nodes will only store their own UDPN transaction data. 
The third-party businesses’ IT systems must use gateway APIs to access the Business Node. This API gateway provides unified digital identity management and payment transaction processing services to the Business Node operators.

Private storage contains the credentials issued by the UDPN issuer or currency systems along with storing off-chain private data, such as that related to KYC. To access credentials, other DIDs need to be granted permission by the Business Node owner. 

The node uses a digital identity service to integrate the UDPN DID client SDK. In order to conduct payment services, the node will interact with the UDPN network to initiate a currency transfer or swap request and to support the querying of the state of its own transactions.
  

## Known issues
- The package name is named using the little camel case nomenclature. 
- The class name has the problem of naming irregularities. 
- Some underlying methods are not commented. 


## Project module
- comp-api-model:The public entity module of the BN-Service. 
- comp-common:The public method module of the BN-Service. 
- bn-gateway：The gateway of the BN-Service is provided to BN-Service externally. 
- redeureka:The registry of the BN-Service. 
- bn-processcore:The core functions of BN-service, including transactions, binding did, independent access to the network, etc. 
- bn-event:The event monitoring service of the BN-Service currently includes monitoring on-chain transactions. 
- bn-init:The initialization module of the BN-Service currently includes the initialization of the database. 

## Precondition
### 1.Module startup sequence
**redeureka -> bn-gateway -> bn-init -> (bn-processcore,bn-event)**

First start redeureka to provide registration services; then start bn-gateway; then start bn-init to initialize data; finally start bn-processcore, bn-event (no order). 

## Quick Start

After cloning the BN-Service to obtain the source jar, you can start the project in the following two ways, **pay attention to the startup sequence of each module**. 

### Start the project directly using the command line, and refer to the README.md under each module for the startup configuration items. 

`java -jar xxxxxx.jar --server.port=8151 --spring.bn-code=xxx`

### Start the project by creating a shell script, and refer to the README.md under each module for the startup configuration items

#### STEP 1.Create shell script in the same directory as the jar package

`start`

```
#!/bin/bash     
nohup java -Xms256m -Xmx512m -jar `pwd`/xxxxxx.jar \
--server.port=8155 \
--spring.vn-code=xxxxx \
 > log.log  2>&1 &
tail -f ./log.log

```

`stop`

```

#!/bin/bash     
PID=$(ps -ef | grep `pwd`/xxxx.jar  | grep -v grep | awk '{ print $2 }')
if [ -z "$PID" ]
then
    echo Application is already stopped
else
    echo kill -9 $PID
    kill -9 $PID
fi

```

### STEP 2.Execute shell script

Startup project

`./start`

Stop project

`./stop`

## contact us

Email: xxxx@reddatetech.com