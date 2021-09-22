# BN-Service - Bn-event

## Configuration example
``` 
--server.port=8056 \
--spring.shardingsphere.datasource.master.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--spring.shardingsphere.datasource.master.username=xxxx \
--spring.shardingsphere.datasource.master.password=xxxxx \
--spring.shardingsphere.datasource.slave.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--spring.shardingsphere.datasource.slave.username=xxxx \
--spring.shardingsphere.datasource.slave.password=xxxxx \
--eureka.client.service-url.defaultZone=http://admin:123456@127.0.0.1:18761/eureka \
--spring.bn-code=UDPN-TEST-BN-1 \
--logging.logpath=d://opcLogs \
--logging.level.root=info \
--spring.rabbitmq.host=eventserver \
--spring.rabbitmq.username=xxxx \
--spring.rabbitmq.password=xxxx \
--spring.rabbitmq.port=5672 \
--spring.rabbitmq.virtual-host=my_vhost \
--spring.rabbitmq.default.host=127.0.0.1 \

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
| spring.bn-code | The code of Tn |
|logging.logpath |Log output address |
|logging.level.root |Log level |
|spring.rabbitmq.host |The address of rabbitmq |
|spring.rabbitmq.username |The username of rabbitmq |
|spring.rabbitmq.password |The password of rabbitmq |
|spring.rabbitmq.port |Rabbitmq port |
|spring.rabbitmq.virtual-host|Connect virtual mq address |
|spring.rabbitmq.default.host|Rabbitmq default host |


