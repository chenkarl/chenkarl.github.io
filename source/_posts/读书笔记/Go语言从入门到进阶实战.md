---
title: 'Go语言从入门到进阶实战读书笔记'
date: 2018-4-19 22:17:00
tags:
---

# 第九章 包
包初始化 init()
# 第十章 并发
goroutine channel
go 函数名（参数列表）{
    函数体
}（调用参数列表）
创建goroutine时，被调用函数的返回值会被忽略
声明
var 通道变量 chan 通道类型
创建
通道实例:= make(chan 数据类型)
通道变量 <- 值
select{
    case :
    case :
    default :
} 
case <-ch
case d:= <-ch
case ch<-100
原子访问 atomic 
互斥锁 sync.Mutex 保证同时只有一个goroutine可以访问共享资源
等待组 sync.WaitGroup 保证再并发环境中完成指定数量的任务

# 第十一章 编译与工具
go build
go test
基准测试 -bench=.
-benchmem 测试内存
go pprof 发现代码性能问题的调用位置

# 第十二章 避坑与技巧
1 goroutine不要滥用，要注意退出与回收资源
2 通道中数据如无作用，仅用来发送通知，则使用等待组代替
3 反射 灵活但低效
* 能使用原生代码，尽量避免反射调用
* 提前缓冲反射值对象，对性能有很大帮助
* 避免反射函数调用，实在需要调用时，先提前缓冲函数参数列表，并且尽量少地使用返回值
4 接口的nil判断
