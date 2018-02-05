## mongo  

https://www.cnblogs.com/best/p/6212807.html

http://www.runoob.com/nodejs/nodejs-mongodb.html

http://www.expressjs.com.cn/starter/hello-world.html

https://coding.net/u/zhangguo5/p/NodeJS002/git

1.use 表名 

2.show dbs  查看数据库

3.db.dropDatebase()   删除表

4.db.products.insert({name:"iphone",price:1988});   插入数据

5.for(var i=0;i<5;i++)db.users.save({'_id':i,'name':'zhangguo'+i,'age':i+8});   批量添加



http://blog.csdn.net/qq_27093465/article/details/54574948

http://blog.csdn.net/grs294845170/article/details/77848114

1.node项目 npm start

2.前端项目webpack-dev-server

3.mongodb    mongod --dbpath=D:\mongodb\data 

   启动mongod mongo





MongoDB Node.js驱动程序是被官方所支持的原生Node.js驱动程序，他是至今为止最好的实现， 并且得到了MongoDB官方的支持。MongoDB团队已经采用MongoDB Node.js驱动程序作为标准方法。

```
npm install mongodb@1.4.3     // MongoDB Node.js驱动程序
npm install mongoose@3.8.8    //mongoose模块12
```

**要从Node.js连接MongoDB数据库我们有两种方法可选择：**

1. 通过实例化mongodb模块中提供的mongodbClient类，然后使用这个实例化的对象来创建和管理mongodb连接；
2. 使用字符串进行连接；