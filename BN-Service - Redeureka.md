# BN-Service - Redeureka

## Configuration example
``` 
--server.port=8762 \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--spring.security.user.name=xxxxx \
--spring.security.user.password=xxxxxx \
--logging.logpath=d://opcLogs \
--logging.level.root=info \
--spring.cloud.gateway.httpclient.websocket.max-frame-payload-length=524288000 \

```


## Configuration instructions

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | Service port |
| eureka.client.service-url.defaultZone |Default address of eureka |
| spring.security.user.name | security username |
| spring.security.user.password | security password |
| logging.logpath | Log output address |
| logging.level.root | Log level |
| spring.cloud.gateway.httpclient.websocket.max-frame-payload-length |Maximum transmission volume of websocket in the gateway |

