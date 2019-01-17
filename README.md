# docker简明教程

## 使用

```bash
# 下载
git clone https://github.com/OMGZui/docker-php.git

# 修改工作目录
APP_CODE_PATH_HOST=

# 运行
docker-compose up -d nginx mysql redis workspace mongo

```

## nginx

在工作目录下建一个index.php，并输入`<?php phpinfo();`

浏览器打开 http://localhost 即可看到php环境

## mysql

```bash
# 密码是root
mysql -h 127.0.0.1 -P 3306 -u root -p

Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 6
Server version: 5.5.62 MySQL Community Server (GPL)

Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.

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
+--------------------+
4 rows in set (0.04 sec)
```

## redis

```bash
# 无密码
redis-cli -h 127.0.0.1 -p 6379

127.0.0.1:6379> ping
PONG
```

## mongodb

```bash
# 无密码
mongo 127.0.0.1:27017

MongoDB shell version v4.0.4
connecting to: mongodb://127.0.0.1:27017/test
Implicit session: session { "id" : UUID("00fa8aca-9ba0-478b-9a78-b7a11e4253f1") }
MongoDB server version: 4.0.5
Server has startup warnings:
2019-01-17T04:02:33.962+0000 I CONTROL  [initandlisten]
2019-01-17T04:02:33.962+0000 I CONTROL  [initandlisten] ** WARNING: Access control is not enabled for the database.
2019-01-17T04:02:33.962+0000 I CONTROL  [initandlisten] **          Read and write access to data and configuration is unrestricted.
2019-01-17T04:02:33.962+0000 I CONTROL  [initandlisten]
---
Enable MongoDB's free cloud-based monitoring service, which will then receive and display
metrics about your deployment (disk utilization, CPU, operation statistics, etc).

The monitoring data will be available on a MongoDB website with a unique URL accessible to you
and anyone you share the URL with. MongoDB may use this information to make product
improvements and to suggest MongoDB products and deployment options to you.

To enable free monitoring, run the following command: db.enableFreeMonitoring()
To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---

>
```