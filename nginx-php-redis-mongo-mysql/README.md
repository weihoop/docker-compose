本项目实现nginx + php-fpm + redis + mysql基础环境

## 版本说明：

- nginx:1.14.0
- php-fpm:7.2
- redis:7.2
- mongo:3.6.7
- mysql:5.7

## 使用说明(mac/centos/ubuntu)

##### 依赖环境：docker、docker-compose


##### 1. 检出git库到本地

##### 2. 运行启动命令
 
``` 
docker-compose up -d
```

##### 3. 根据项目需要,修改配置(一般小项目不需要修改)

- nginx和php-fpm 目录挂载为同一目录
- 各容器服务的web、日志、DB目录，自动映射到本地目录（持久化）

##### 4. 暴露端口
   
- nginx: 8080
- redis: 6379  (无密码验证，注意安全)
- mongo: 27017 (无密码验证，注意安全)
- mysql: 3306

##### 5. 数据库密码

- mysql: root密码见Dockerfile，可根据需要进行修改。
- redis: 无密码，建议更换本地映射端口为其它端口
- mongo: 无密码，建议更换本地映射端口为其它端口

##### 6. 访问方式

- nginx: 127.0.0.1:8080
- redis: 127.0.0.1:6379
- mongo: 127.0.0.1:27017
- mysql: 127.0.0.1:3306

##### 7. 测试方法

```
# curl 127.0.0.1:8080/test.php
Halo php-fpm!
```
