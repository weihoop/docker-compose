本项目实现nginx + php-fpm基础环境

## 版本说明

- nginx:1.14.0
- php-fpm:7.2

## 使用说明(mac/centos/ubuntu)

##### 依赖环境：docker、docker-compose


##### 1. 检出git库到本地

##### 2. 运行启动命令

```
docker-compose up -d
```

#####  3. 根据项目需要,修改配置(一般小项目不需要修改)

- nginx和php-fpm 代码挂载为同一目录
- 各容器服务的web、日志、DB目录，自动映射到本地目录（持久化）
- redis、mysql、mongo服务，需要单独部署

##### 4. 暴露端口

- nginx: 8080

##### 5. 访问方式

- nginx: 127.0.0.1:8080

##### 6. 测试方法

```
# curl 127.0.0.1:8080/test.php
Halo php-fpm!
```
