# docker集群管理

## 可视化

```bash
docker service create --name portainer --publish 9000:9000 --replicas=1 --constraint 'node.role == manager' --mount type=bind,src=//var/run/docker.sock,dst=/var/run/docker.sock --mount type=bind,src=//opt/portainer,dst=/data portainer/portainer -H unix:///var/run/docker.sock

```

## swarm集群

```bash
# 创建集群
docker swarm init --advertise-addr 192.168.101.132

# 加入集群
docker swarm join --token SWMTKN-1-24xt0w9dh5rbdiotgzyy8rlhy0ow613tox00wjgsbafwlj65us-3ghoxfn9kiwakwkn71xfk32b5 192.168.101.132:2377
```

