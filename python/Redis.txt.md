# Redis
#python #Redis

```
sudo service redis-server start 启动数据库服务

redis-cli  //链接到数据库

SET key value 设置键值；
EXISTS key 判断键是否存在；
EXPIRE key seconds 设置 Key 的过期时间，过期以后Key 将被自动删除；
TTL key 获取 Key 的剩余生存时间；
DEL key 删除 Key；
TYPE key 获取 Key 对应的 Value 的类型；

```


[image:879727A3-042B-4E89-BDCA-C35060A3E6A7-2529-000379D41E7D8A59/93C4B3BE-BB6D-44AB-8C6B-1653DDC36C6F.png]
哈希类型的键值
HSET key field value 设置名称为 key 的哈希的字段 field 为值 value；
HMSET key filed value field value
为多个字段赋值
HGET key field 获取名为 key 的哈希的字段 field;
HGETALL key 获取名为 Key 的哈希所有字段和 Value;
HKEYS key 获取名为 Key 的哈希的所有字段；
HLEN key 获取名为 Key 的哈希的字段数量

Redis 还支持有序集合，有序集合可以用于快速实现排名功能，主要的操作指令如下：
ZADD key score member 将成员和对应的评分添加到有序集合中；
ZREVRANK key member 获取 member 在有序集合 key 中的排名；
[image:B3F05B03-9BAD-427D-B068-AB2397845953-2529-00037A337631D8C1/3335D16B-A9BB-4473-90E9-0BB7C99372F4.png]

面例子中，我们通过 ZADD 往 rank 中添加了三个成员，最后通过 ZREVRANK 依次获取了成员的排名，可以发现排名是从 0 开始计算的，排第 0 的成员得分最高。有序集合的排名，还有 zrank 方法，请大家自行试验结果

列表
[image:B950254B-78E6-457F-92B2-7E20EF40D826-2529-00037A44849EB91E/136F4DEA-5ACB-48EB-ABFE-ABE0DDFEF45F.png]

集合类型
[image:6C0CB67A-A90F-44C9-9F49-2B1AC459D353-2529-00037A4F22E2FE9F/561B2498-C605-416E-B026-5D78F259E1C4.png]




