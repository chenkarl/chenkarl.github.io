---
title : 'redis使用笔记'
date : 2018-09-12 09:44:00
tags : 学习笔记
---

set(key,value);
set(key,value,'EX',time);

EX seconds -- Set the specified expire time, in seconds.
PX milliseconds -- Set the specified expire time, in milliseconds.
NX -- Only set the key if it does not already exist.
XX -- Only set the key if it already exist.

setex(key,ex,value);
get(key);
del(key);
exists(key);

