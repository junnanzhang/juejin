# Mongodb
#python #mongodb

```
	启动环境
	sudo service mongod start

	链接数据库
	mongo

打造单独的环境
sudo pip install virtualenv
$ virtualenv -p /usr/bin/python3.5 env
$ source env/bin/activate
$ pip install pymongo ipython

use shiyanlou //使用shiyanlou表

db.user.insertOne({name: "Aiden", age: 30, email: "luojin@simplecloud.cn", addr: ["CD", "SH"]})

show databases; 显示数据库

show collections; 显示表

```

插入多条
[image:C6A9B291-6C9C-4A18-8AA2-93B62BC4B1CF-2529-000376FF23AB3979/908BE5D8-2CEF-4273-AE34-F4F6AA1CC66F.png]

查找
[image:A5AB9B64-6FE3-4013-B723-4221F9D926D4-2529-0003770D2A1174A6/46C7FC54-8855-42DA-BC74-EB7759007A17.png]
更新数据
[image:961EE230-C78D-4ABA-9F96-010237826BAB-2529-0003771BC131C9C5/71AEBAC0-4E1B-467E-A2CE-F78E0F7FAE32.png]

删除数据

[image:12885F85-A01C-4F3B-913E-FE7688290817-2529-0003772FCCA0B2D1/BDA39CAC-1CD0-4602-99A1-5D5434AD796F.png]