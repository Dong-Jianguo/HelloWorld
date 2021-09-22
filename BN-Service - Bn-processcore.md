# BN-Service - Bn-processcore

## Configuration example
``` 
--server.port=18082 \
--spring.shardingsphere.datasource.master.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--spring.shardingsphere.datasource.master.username=xxxx \
--spring.shardingsphere.datasource.master.password=xxxxxx \
--spring.shardingsphere.datasource.slave.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--spring.shardingsphere.datasource.slave.username=xxxx \
--spring.shardingsphere.datasource.slave.password=xxxxxx \
--eureka.client.service-url.defaultZone=http://admin:123456@127.0.0.1:18761/eureka \
--vn.ribbon.listOfServers=127.0.0.1:8081 \
--spring.tn-code=VN111100009,VN111100009 \
--spring.tn-did=did:udpn:2JtdUh3ZL7FNSdMZyUkBVw6Jo4yG,udpn:2JtdUh3ZL7FNSdMZyUkBVw6Jo4yGGGG \
--did.proxy.properties.file=/bsn/udpn_bn/processing_bn/application-bn-besu.properties \
--spring.rabbitmq.default.host=127.0.0.1 \
--logging.logpath=d://opcLogs \
--logging.level.root=info \

```


## Configuration instructions

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | Service port |
| mysql.smart.url | Master database address |
| mysql.smart.username | Master database user name  |
| mysql.smart.password | Master database password |
| mysql.slave.url |Slave database address |
| mysql.slave.username |Slave database user name |
| mysql.slave.password | Slave database password|
| eureka.client.service-url.defaultZone | Default address of eureka |
|vn.ribbon.listOfServers |vn instance address |
|spring.tn-code | The code of tn, separated by commas|
|spring.tn-did |The did of tn, separated by commas |
|did.proxy.properties.file |did profile address |
|spring.rabbitmq.default.host |rabbit mq default host |
|logging.logpath |Log output address |
|logging.level.root |Log level |


