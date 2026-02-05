# 115网盘自动订阅工具
网盘订阅工具，支持115

## 镜像

最新镜像版本地址：[https://cnb.cool/cloud115/cloudsubbot/-/packages/docker/cloudsubbot](https://cnb.cool/cloud115/cloudsubbot/-/packages/docker/cloudsubbot)

```
docker pull docker.cnb.cool/cloud115/cloudsubbot:latest
```

运行：
```
docker run -v /database:/database -d -p 9114:9114 镜像ID
```

docker-compose
```
services:
  cloudsubbot:
    image: docker.cnb.cool/cloud115/cloudsubbot:latest
    platform: linux/amd64
    container_name: cloudsubbot
    restart: unless-stopped
    ports:
      - "9114:9114"
    environment:
      - ENV=production
      - DB_PATH=/database/sqlite.db
      - TZ=Asia/Shanghai
    volumes:
      - ./database:/database
```

## 使用教程

### 配置115网盘配置

#### 授权配置
配置调用open api权限， 截图通过115app进行扫描，点击【已扫描】即可

#### COOKIE配置
需要通过115cookie后，才可以进行转存分享的链接

#### 根目录配置
配置115网盘文件的cid

## 添加QQ群联系群主咨询服务
