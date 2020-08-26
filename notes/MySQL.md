## MySQL {docsify-ignore}

- 常规命令
  - 进入数据库软件：`mysql -u root -p`
  - 创建数据库：` CREATE DATABASE [database-name];`
  - 删除数据库：`DROP DATABASE [database-name]`
  - 查询可用的数据库：`SHOW DATABASES;`
  - 切换到指定数据库：`USE [database-name];`
  - 查询当前数据库下的所有表：`SHOW TABLES;`
  - 显示表结构：`DESCRIBE [table-name];`，简写`DESC [table-name];`
  - 在当前数据库下创建表：`CREATE TABLE [table-name](name VARCHAR(20),sex CHAR(1));`
  - 删除表：`DROP TABLE [table-name];`
  - 查看创建表时的SQL语句：`SHOW CREATE TABLE [table-name];`
  
---
