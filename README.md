# Simple Openresty Nginx with simple syslog-server 

## Use it to send Nginx modified access-logs to syslog on port 9898 UDP

## Setup
- docker-compose
```
docker-compose up -d
```

## Watch the events

- navigate on browser to localhost:8080/no-such-page

```
docker logs -f nginx-test-rig_syslog_1
```

## To generate syslog-server docker image

- Clone git repo [mondbev1/simple-syslog-server](https://github.com/mondbev1/simple-syslog-server)

```
docker build -t syslog-server syslog-server-udp .
docker push ...
```