---
title : 'Node.js学习笔记'
date : 2018-05-14 09:44:00
tags : 学习笔记
---

# 一、概念理解
原型链：
    原型对象：可以作为一个模板，新对象可以从中获取原始的属性。
    任何对象都可以指定自身的属性，既可以编译时创建也可以在运行时创建。
    任何对象都可以作为另一个对象的原型k，从而允许后者共享前者的属性。
    _proto_属性会指向函数对象的原型对象，由_proto_属性串起来直到null的链叫做原型链。

作用域链：
    根据在内部函数可以访问外部函数变量的这种机制，用链实查找决定哪些数据能被内部函数访问。
词法作用域：
语法树：
上下文：
    挂载变量与函数的对象。
this:
    函数中调用为全局对象，浏览器中为window对象。
变量对象：执行环境中的变量和函数的总称叫做变量对象。
活动对象：活动对象就是作用域链上正在被执行和引用的变量对象。
垃圾回收：
闭包：内部函数的作用域链仍保持着对父函数活动对象的引用。
    作用:1、可以读取自身外部的变量。2、让这些外部变量始终保存在内存中。   
回调：将一个函数作为参数传递给另一个函数，并且在第一个函数完成后被调用。

# 二、操作

1、npm install [moudle name]
本地安装模块
npm install -g [moudle name]
全局安装模块

# 其他
node 解决并发依靠的是事件化的I/O模型

js   只要在函数内部定义一个局部变量，函数在解析的时候都会将这个变量提前声明。
    函数内部声明变量一定要用var，如果不用实际上就是声明一个全局变量。

express

## 连接MongoDb
> 使用Mongoose
可以监听的事件：open,error,disconnected,connected(这个能不能监听。。。。)

## 原则
1、不阻塞。因为node是单线程的。
2、快速返回。如果不能快速返回，就应当将其移进另一个线程中。
# 测试
Vows

Mocha

总结：

# nvm 管理node版本
内网

[解决方案](https://my.oschina.net/u/3305487/blog/1538289)
nvm ls
列出所有node版本
nvm use v7.8.0
切换版本

# 中间件
用途：验证，日志记录，缓存异常通知，重定向
next()将请求和响应对象传递到下一个中间件（如果是最后一个中间件，就是应用程序逻辑），使用res.end()返回响应。

# Redis
## Redis设为系统服务
redis-server --service-install redis.windows.conf

# Egg
ejs引擎没有增加csrf验证

# Mongoose类型
ObjectId
String
Number
Date
Buffer
Boolean

设默认值 default

egg 设置代理
[解决方案](https://eggjs.org/zh-cn/core/httpclient.html#调试辅助)
注：最后命令启动 http_proxy=http://127.0.0.1:8888 npm run dev 可写成bat脚本

curl请求中，中文必须经过encodeURI(keywords)编码后才可以正确传输，否则会变成异常字符

问题：事件监听，未发生响应事件，请求已经返回
node http请求后，里面的事件监听响应如何实现
使用promise包装

