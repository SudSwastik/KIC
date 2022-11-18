# Kong Ingress Controller

> Steps To enable Admin API In KIC

> Update Deployment Admin Key "KONG_ADMIN_LISTEN" with 8001 port

```
$ - name: KONG_ADMIN_LISTEN
    value: 0.0.0.0:8001, 127.0.0.1:8444 http2 ssl reuseport backlog=16384
```

> Update Service With New Port

```
$   
    - name: admin
      port: 8001
      protocol: TCP
      targetPort: 8001
    - name: admin-ssl
      port: 8444
      targetPort: 8444
      protocol: TCP
```
