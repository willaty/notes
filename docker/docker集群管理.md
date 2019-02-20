# docker集群管理

## 可视化

```bash
$ curl -L https://downloads.portainer.io/portainer-agent-stack.yml -o portainer-agent-stack.yml

$ docker stack deploy --compose-file=portainer-agent-stack.yml portainer
```

## swarm集群

```bash
# 创建集群
docker swarm init --advertise-addr 192.168.101.132

# 加入集群
docker swarm join --token SWMTKN-1-24xt0w9dh5rbdiotgzyy8rlhy0ow613tox00wjgsbafwlj65us-3ghoxfn9kiwakwkn71xfk32b5 192.168.101.132:2377
```

