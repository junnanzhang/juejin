# SQLAlchemy  IPython
#python

Ipython  
ctrl + z  暂停 iPython
fg 恢复 ipython

```
from sqlalchemy import create_engine

```

[image:5E59D6DE-D4F7-47F4-A4EE-A21B2189F5A6-2529-00036C1A3D230F16/55AF3CEB-9783-437D-97C7-A170AC234879.png]
declarative_base
from sqlalchemy.ext.declarative import declarative_base

[image:533E3076-7DFB-4F90-97B8-B571531CA0AE-2529-00036C39AD6DF5C3/5604B3DB-1E60-46B9-BBCF-4C0792F45E86.png]

[image:CB1D6905-BD37-4C5E-87E4-595BA7AF78CB-2529-00036C3C58462369/D3783457-98E7-406D-A81B-EB47AAC93B9E.png]

[image:FB73801B-29E0-4D5B-B6AA-2599B608536B-2529-00036C4A92F84EE4/B9C6ED2C-9A48-4203-83B8-D3BE83E8193B.png]
如果想通过 User 查询数据库该怎么办呢？需要先引入 Session。Session 是映射类和数据库沟通的桥梁，包含事务管理功能。通过以下代码创建 Session:

[image:8606185B-F724-4DDF-BD43-30388A43D093-2529-00036C4F8CC3322F/A76BC901-4C6B-40F8-A3A2-B6FD4B4536B5.png]

[image:ECD706DC-F447-43ED-A732-FC10D52682DD-2529-00036C5EA4F88118/A0ADAA47-77C4-4AC7-B2B3-B372E49F5D41.png]
上面的查询过程中我们使用到了 filter 对数据进行筛选。filter 中的运算符可以填入 SQL WHERE 子句中的运算符（像 ==, !=, >, < 等），或者是 AND, OR 等运算符。另外，这里的 filter 也可以更换为 filter_by 函数，后者相对于()没有那么灵活，一般会推荐使用 filter。

[image:E5B94071-8AF5-4D16-9B66-A592FEF06E3E-2529-00036CAFFE30A46A/E6CF1455-0FFC-4734-A636-4B07D3A11EAD.png]
[image:1C6F2C2D-5F5F-4FCD-90A9-5BA361D76506-2529-00036CB9F1A5BAB3/773385A8-E22B-4A75-87FC-4D53E68201F6.png]
String(60), nullable = False 非空
创建表
[image:AD32406D-0246-4470-942C-90D193204C0F-2529-00036CC68F35FE76/206FE10C-5254-4832-8036-BE6737C632B7.png]

CRUD
查询
course = session.query(Course).first()
建对象
lab1 = Lab(name='ORM 基础', course_id=course.id)
lab2 = Lab(name='关系数据库', course=course)
session.add(lab1)
session.add(lab2)
session.commit()
更新数据库
course.name = 'Python 数据分析'
session.add(course)
session.commit()

Delete
session.delete(lab1)
session.commit()
course.labs
1对多 关系 多对多关系
1对1
[image:4401D698-3C02-424F-A8D4-987B2A9CD06B-2529-0003711C40C111DE/5FF9AD37-58E6-4F8F-866C-5F957A249598.png]
如果两张表对于同一张表（假如表名是 T）都是 1:M 的关系，那么就可以把 T 当做中间表，创建出两张表的多对多关系。比如课程表和标签表的关系，可以由以下代码创建
[image:41C66380-5DD2-4403-B841-257278A7B876-2529-0003713615D2466F/55E77A3C-5115-4886-A330-DC992A67D07A.png]


[image:E78F1CDB-B240-44BE-A709-259103AC773D-2529-00037141768AD669/D6774731-659E-4D26-92E3-9962A2C222BC.png]

[image:43D4D66E-530A-4754-AF66-BB4FE5922583-2529-00037154F0857D9F/E4F72A74-011B-4A47-BCBA-DAE7FFFCB595.png]