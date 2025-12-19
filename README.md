# OPS

## 1. DataBase
### 1.1 Redis
### 1.2 MySQL
### 1.3 MongoDB
### 1.4 PostgreSQL

## 2. Gitea


## Clash
> 兜底方案

```bash
# 保存镜像
podman save --format oci-archive  -o clash_core.oci  docker.io/metacubex/mihomo
podman save --format oci-archive  -o clash_web.oci  ghcr.io/zephyruso/zashboard

# 加载镜像
podman load -i ./img/clash_core.oci 
podman load -i ./img/clash_web.oci 


# 设置代理
export http_proxy=http://127.0.0.1:7890
export https_proxy=http://127.0.0.1:7890
export all_proxy=socks5://127.0.0.1:7890

# 取消代理
unset http_proxy https_proxy all_proxy

#永久生效
sudo vim /etc/environment
#写入
http_proxy=http://127.0.0.1:7890
https_proxy=http://127.0.0.1:7890
all_proxy=socks5://127.0.0.1:7891

```