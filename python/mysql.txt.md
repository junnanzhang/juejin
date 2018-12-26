# mysql
#python #mysql
```
启动mysql
sudo service mysql start
安装mysqlclient
sudo pip3 install mysqlclient

链接数据库
mysql -u root

基本数据库操作
show databases;
create database <db_name>;
drop database <db_name>;

链接到数据库
use <database>;

创建表结构
CREATE TABLE 表的名字
(
列名a 数据类型(数据长度),
列名b 数据类型(数据长度)，
列名c 数据类型(数据长度)
);

显示表
show tables;

如果想查看一张表的字段信息，可以通过 
show create table <table_name>; 
或者 describe <table_name>;

插入数据
insert into 标的名字（列名a, 列名b， 列名c） values(值1， 值2， 值3)

删除
delete from user where id = 3;

查询
select * from <table_name>;


```
约束
```
alter指令 修改表的字段
alter table <table_name> modify <列名> varchar(64) unique; 
alter table user add constraint unique(email) <列名>

外键约束创建时，必须要求另一张表中存在主键，主键在表中能唯一的确定某一行的值。

alter table user add constraint pk_id primary key (id);

create table course 
    -> (
    -> id int(10) auto_increment,
    -> name varchar(64),
    -> teacher_id int(10),
    -> primary key (id),
    -> constraint fk_user foreign key (teacher_id) references user(id)
    -> );

联合查询
select * from course join user on course.teacher_id = user.id;

```