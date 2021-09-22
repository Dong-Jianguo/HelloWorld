# VN-Service - Vn-init

## Configuration example
``` 
--server.port=18255 \
--mysql.smart.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--mysql.smart.username=xxxxx \
--mysql.smart.password=xxxxx \
--mysql.slave.url="jdbc:mysql://127.0.0.1:3306/network_udpn_bn" \
--mysql.slave.username=xxxxx \
--mysql.slave.password=xxxxx \
--eureka.client.service-url.defaultZone=http://admin:123456@127.0.0.1:18761/eureka \
--vn.init.file.path=/bsn/vninit.yml \

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
| vn.init.file.path | init file path |


