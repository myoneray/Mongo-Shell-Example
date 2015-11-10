
### Shell-Mongo-Example
```

```
连接数据库
```

▶ mongo
MongoDB shell version: 2.4.9
connecting to: test

```
显示当前连接的ＤＢ
```
> db
test

```
显示当前DB的所有集合
```
> show dbs
anti_cheat	0.203125GB
anu	0.203125GB
day1110-1	0.203125GB
test	0.203125GB

```
进入该ＤＢ　 **`day1110-1`**
```

> use day1110-1
switched to db day1110-1
```
删除该ＤＢ　 **`day1110-1`**　哈哈哈w(@。@;)w
```
> db.dropDatabase();
{ "dropped" : "day1110-1", "ok" : 1 }
```
看　 **`day1110-1`**　不见了吧　ʅ(‾◡◝)ʃ【得瑟】
```
> show dbs
anti_cheat	0.203125GB
anu	0.203125GB
test	0.203125GB

```
进入正题　操作**`Ｔｅｓｔ`**
```

> use test
switched to db test

> show  collections
myTest
mycol
mytable
system.indexes
> db
test

```
### 插入一条数据
```
> db.col.insert({title: 'MongoDB 教程', 
...     description: 'MongoDB 是一个 Nosql 数据库',
...     by: '麦子教程',
...     url: '想嘻嘻嘻嘻嘻嘻',
...     tags: ['mongodb', 'database', 'NoSQL'],
...     likes: 100
... })
```
### 查找所有数据
```
> db.col.find();
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
```
### 插入许多条数据
```
> db.col.insert({title: 'MongoDB 教程',     description: 'MongoDB 是一个 Nosql 数据库',     by: '麦子教程',     url: '想嘻嘻嘻嘻嘻嘻',     tags: ['mongodb', 'database', 'NoSQL'],     likes: 100 })
> db.col.insert({title: 'MongoDB 教程',     description: 'MongoDB 是一个 Nosql 数据库',     by: '麦子教程',     url: '想嘻嘻嘻嘻嘻嘻',     tags: ['mongodb', 'database', 'NoSQL'],     likes: 100 })
> db.col.insert({title: 'MongoDB 教程',     description: 'MongoDB 是一个 Nosql 数据库',     by: '麦子教程',     url: '想嘻嘻嘻嘻嘻嘻',     tags: ['mongodb', 'database', 'NoSQL'],     likes: 100 })
> db.col.insert({title: 'MongoDB 教程',     description: 'MongoDB 是一个 Nosql 数据库',     by: '麦子教程',     url: '想嘻嘻嘻嘻嘻嘻',     tags: ['mongodb', 'database', 'NoSQL'],     likes: 100 })

```
### 查找所有数据
```
> db.col.find();
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419104266eb3dc31bcd10b"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419107266eb3dc31bcd10c"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
```
### 总条数
```
> db.col.count();
12

```
### 更新第一条数据
**在最后一条**
```
>  db.col.update({"title":"MongoDB 教程"},{$set:{"title":"updateMongoJiaoCheng"}}); 
> db.col.find();
{ "_id" : ObjectId("56419104266eb3dc31bcd10b"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419107266eb3dc31bcd10c"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910e266eb3dc31bcd10f"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd110"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd111"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd112"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd113"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419111266eb3dc31bcd114"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419112266eb3dc31bcd115"), "title" : "MongoDB 教程", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "by" : "麦子教程", "description" : "MongoDB 是一个 Nosql 数据库", "likes" : 100, "tags" : [  "mongodb",  "database",  "NoSQL" ], "title" : "updateMongoJiaoCheng", "url" : "想嘻嘻嘻嘻嘻嘻" }


```
### 更新所有符合`{"title":"MongoDB 教程"}`的数据
```
> db.col.update({"title":"MongoDB 教程"},{$set:{"title":"mongoUpdateAll"}},{multi:true});
> db.col.find();
{ "_id" : ObjectId("56419104266eb3dc31bcd10b"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419107266eb3dc31bcd10c"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910e266eb3dc31bcd10f"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd110"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd111"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd112"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd113"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419111266eb3dc31bcd114"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419112266eb3dc31bcd115"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "by" : "麦子教程", "description" : "MongoDB 是一个 Nosql 数据库", "likes" : 100, "tags" : [  "mongodb",  "database",  "NoSQL" ], "title" : "updateMongoJiaoCheng", "url" : "想嘻嘻嘻嘻嘻嘻" }

```
### 更新所有符合`{"_id":ObjectId("56419112266eb3dc31bcd115")`的唯一一条数据
```
> db.col.save({"_id" : ObjectId("56419104266eb3dc31bcd10b"),"tittle":"UpdateByID"});
> db.col.find();
{ "_id" : ObjectId("56419104266eb3dc31bcd10b"), "tittle" : "UpdateByID" }
{ "_id" : ObjectId("56419107266eb3dc31bcd10c"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910e266eb3dc31bcd10f"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd110"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd111"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd112"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd113"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419111266eb3dc31bcd114"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419112266eb3dc31bcd115"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "by" : "麦子教程", "description" : "MongoDB 是一个 Nosql 数据库", "likes" : 100, "tags" : [  "mongodb",  "database",  "NoSQL" ], "title" : "updateMongoJiaoCheng", "url" : "想嘻嘻嘻嘻嘻嘻" }
```
### 再来一次　（ ＴДＴ）　更新所有符合`{"_id":ObjectId("56419107266eb3dc31bcd10c")`的唯一一条数据
```
> db.col.save({"_id" : ObjectId("56419107266eb3dc31bcd10c"),"tittle":"UpdateByID"});
> db.col.find();
{ "_id" : ObjectId("56419104266eb3dc31bcd10b"), "tittle" : "UpdateByID" }
{ "_id" : ObjectId("56419107266eb3dc31bcd10c"), "tittle" : "UpdateByID" }
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910e266eb3dc31bcd10f"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd110"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd111"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd112"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd113"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419111266eb3dc31bcd114"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419112266eb3dc31bcd115"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "by" : "麦子教程", "description" : "MongoDB 是一个 Nosql 数据库", "likes" : 100, "tags" : [  "mongodb",  "database",  "NoSQL" ], "title" : "updateMongoJiaoCheng", "url" : "想嘻嘻嘻嘻嘻嘻" }

```
### 删除更新的那两条数据　川´･ω･`川
```
> db.col.remove({"tittle":"UpdateByID"});
> db.col.find();
{ "_id" : ObjectId("56419108266eb3dc31bcd10d"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419108266eb3dc31bcd10e"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910e266eb3dc31bcd10f"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd110"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("5641910f266eb3dc31bcd111"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd112"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419110266eb3dc31bcd113"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419111266eb3dc31bcd114"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("56419112266eb3dc31bcd115"), "title" : "mongoUpdateAll", "description" : "MongoDB 是一个 Nosql 数据库", "by" : "麦子教程", "url" : "想嘻嘻嘻嘻嘻嘻", "tags" : [  "mongodb",  "database",  "NoSQL" ], "likes" : 100 }
{ "_id" : ObjectId("564190b0266eb3dc31bcd10a"), "by" : "麦子教程", "description" : "MongoDB 是一个 Nosql 数据库", "likes" : 100, "tags" : [  "mongodb",  "database",  "NoSQL" ], "title" : "updateMongoJiaoCheng", "url" : "想嘻嘻嘻嘻嘻嘻" }
```
### 删除所有的数据　(#+_+)
```
> db.col.remove({});
```
### 没了吧　"o((>ω< ))o"
```
> db.col.find();

```
