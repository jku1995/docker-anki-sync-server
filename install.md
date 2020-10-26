> 更新镜像
1. docker kill 运行的server
2. docker rmi 原来的镜像
3. docker pull　最新的镜像
> 运行镜像
```bash
docker run -itd \
-p "$HOST_PORT":27701 \
--name anki-container \
--restart always \
$DOCKER_IMAGE
```
> 进入镜像
```bash
docker exec -it $container-id /bin/sh
```
> 添加用户

进入镜像之后
```bash
./ankisyncctl.py add user $username
#根据提示输入密码，用于登录anki客户端
```


