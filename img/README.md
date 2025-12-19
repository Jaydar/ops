# img
```
podman save --format oci-archive  -o clash_core.oci  docker.io/metacubex/mihomo
podman save --format oci-archive  -o clash_web.oci  ghcr.io/zephyruso/zashboard

podman load -i ./img/clash_core.oci 
podman load -i ./img/clash_web.oci 

```