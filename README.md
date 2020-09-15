# GRAYLOG

## Starter for beginners

> [https://docs.graylog.org/en/3.3/pages/installation/docker.html](https://docs.graylog.org/en/3.3/pages/installation/docker.html)

## How to persist on GKE

> [https://portworx.com/run-ha-elasticsearch-elk-google-kubernetes-engine/](https://portworx.com/run-ha-elasticsearch-elk-google-kubernetes-engine/)

> You can see how to create Storage Class for GKE PersistentVolumeClaim [https://youtu.be/qktFhjJmFhg?t=1189](https://youtu.be/qktFhjJmFhg?t=1189)

## To test send log into graylog 

```
curl -XPOST http://<LOAD_BALANCER_IP>:12201/gelf -p0 -d '{"short_message":"Hello there", "host":"alpine-k8s.org", "facility":"test", "_foo":"bar"}';
```

## How to initial
1) create kubernetes's objects for graylog
  - graylog
  - mongo (for keeping graylog's configuration)
  - elastic (for keeping graylog's data & logs)
```
to create please use this command 

  kb apply -f k8s
```
