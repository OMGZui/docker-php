# docker-php

建议：先下载好PHP扩展，可以减少请求时间。缺点就是更新不及时

Suggestion: Download the extensions first, that would reduce compile times. But it not the newest.

## Usage

```bash
git clone https://github.com/OMGZui/docker-php.git
cd docker-php
docker-compose up -d mysql nginx redis mongo phpmyadmin memcached

It only need a cup of tea time when network is fast.

```

## Document

本项目抄袭自https://github.com/laradock/laradock 进行了相当的精简。

The project copy the https://github.com/laradock/laradock and simplified.

- phpmyadmin

浏览器打开http://localhost:8080/ 服务器填写mysql，用户名root，密码root

Open the browser and input  http://localhost:8080/ , host is mysql, user is root, password is root.

- redis

```bash
# 默认密码为空 default password is null
docker-compose exec redis bash
redis-cli
127.0.0.1:6379> ping
PONG
```

- mongo

```bash
mongo

MongoDB shell version v3.4.10
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.4.10
Server has startup warnings:
2018-01-09T07:02:16.674+0000 I CONTROL  [initandlisten]
2018-01-09T07:02:16.674+0000 I CONTROL  [initandlisten] ** WARNING: Access control is not enabled for the database.
2018-01-09T07:02:16.674+0000 I CONTROL  [initandlisten] **          Read and write access to data and configuration is unrestricted.
2018-01-09T07:02:16.674+0000 I CONTROL  [initandlisten]

> show databases;
admin  0.000GB
local  0.000GB
```

- nginx

```bash
docker-compose exec nginx bash
如果失败
docker-compose exec nginx ash

```

- mysql

```bash
docker-compose exec mysql bash

mysql -u root -p
Enter password: root

Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 69
Server version: 5.7.20 MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| default            |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.02 sec)
```
