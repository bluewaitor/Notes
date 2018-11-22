# MySQL基础

## 安装

使用`Docker`的`mysql`镜像，使用Docker命令`docker pull mysql`下载MySQL最新的镜像

执行`docker run --name mysql-playground --env MYSQL_ALLOW_EMPTY_PASSWORD=yes --publish 3306:3306 --detach mysql`命令启动一个MySQL的容器。

使用`docker exec -it mysql-playground /bin/bash`进入容器

## 连接MySQL服务和退出

```shell
root@85995aa8dad4:/# mysql -h 127.0.0.1 -u root -p
Enter password:
```

- `-h`指定连接主机
- `-u`指定连接用户名
- `-p`使用密码

输入密码，进入之后显示为：

```bash
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 17
Server version: 8.0.12 MySQL Community Server - GPL

Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

退出的话很简单，直接输入

```bash
mysql> QUIT
Bye
```

按下回车即可。  

退出方法：

- `QUIT`
- `exit`
- `Ctrl + D`

## 输入查询

```bash
mysql> SELECT VERSION(), CURRENT_DATE;
+-----------+--------------+
| VERSION() | CURRENT_DATE |
+-----------+--------------+
| 8.0.12    | 2018-09-28   |
+-----------+--------------+
1 row in set (0.00 sec)
```

- 查询语句通常由一个SQL语句后面跟着分号组成（有的表达式不需要分号，比如前面的`QUIT`）
- 当你发出查询时，mysql将其发送到服务端执行并显示结果，然后打印另一个`mysql>`提示符表示它已准备好进行另一个查询。
- mysql以表格形式（行和列）显示查询输出。第一行包含列的标签。以下行是查询结果。通常，列标签是从数据库表中提取的列的名称。如果您正在检索表达式的值而不是表列（如刚刚显示的示例中所示），则mysql使用表达式本身标记列。
- mysql显示返回了多少行以及执行查询所需的时间，这使您可以大致了解服务器性能。这些值是不精确的，因为它们代表挂钟时间（不是CPU或机器时间），并且因为它们受到服务器负载和网络延迟等因素的影响。

mysql关键字大小写不区分。以下查询是等效的：

```shell
mysql> SELECT VERSION(), CURRENT_DATE;
mysql> select version(), current_date;
mysql> SeLeCt vErSiOn(), current_DATE;
```

mysql也可以用来做一些简单的计算：

```shell
mysql> SELECT SIN(PI()/4), (4+1)*5;
+--------------------+---------+
| SIN(PI()/4)        | (4+1)*5 |
+--------------------+---------+
| 0.7071067811865475 |      25 |
+--------------------+---------+
1 row in set (0.00 sec)
```

## 创建和使用数据库

使用`SHOW`语句显示服务端拥有的数据库：

```shell
mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.00 sec)
```

使用`USE`语句访问数据库：

```shell
mysql> USE mysql
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
```

### 创建和选择一个数据库

创建一个menagerie数据库

```shell
mysql> CREATE DATABASE menagerie;
Query OK, 1 row affected (0.08 sec)
```

使用menagerie数据库

```shell
mysql> USE menagerie
Database changed
```

> 注意，上面这条语句可以不使用分号

我们也可以在进入会话的时候指定使用的数据库

```shell
shell> mysql -h host -u user -p menagerie
Enter password:
```

> 注意，menagerie不是密码，如果要直接输入密码的话，密码和p之间不需要空格。

查看当前所用的数据库

```shell
mysql> SELECT DATABASE();
+------------+
| DATABASE() |
+------------+
| menagerie  |
+------------+
1 row in set (0.00 sec)
```

### 创建一个表

```shell
mysql> SHOW TABLES;
Empty set (0.00 sec)
```

可以知道，当前我们是没有表的。接下来，我们来创建一个表。

```shell
mysql> CREATE TABLE pet (name VARCHAR(20), owner VARCHAR(20), species VARCHAR(20), sex CHAR(1), birth DATE, death DATE);
Query OK, 0 rows affected (0.08 sec)
```

再使用`SHOW TABLES;`

```shell
mysql> SHOW TABLES;
+---------------------+
| Tables_in_menagerie |
+---------------------+
| pet                 |
+---------------------+
1 row in set (0.01 sec)
```

可以看到，我们创建了一个`pet`表。

查看下创建的表详情

```shell
mysql> DESCRIBE pet;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| name    | varchar(20) | YES  |     | NULL    |       |
| owner   | varchar(20) | YES  |     | NULL    |       |
| species | varchar(20) | YES  |     | NULL    |       |
| sex     | char(1)     | YES  |     | NULL    |       |
| birth   | date        | YES  |     | NULL    |       |
| death   | date        | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
6 rows in set (0.00 sec)
```

### 给表添加数据
