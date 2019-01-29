# Go语言
切片是可变长的数组

[导入github包]()

go get 包的地址

自己创建的包，放在相同的文件夹的名字下

should have comment or be unexported:有这个警告意味着被包外调用的函数或变量应该有注释

Go Web 框架
iris
beego
beego默认生成文件在gopath路径下，因此，路由找不到有可能是main.go中的路由路径引用的是gopath下的路由文件。

beego.debug()打日志 error 等
参数传入失败原因！！！
如果要忽略一个字段，有两种办法，一是：字段名小写开头，二是：form 标签的值设置为 -
任何需要对外暴露的名字必须以大写字母开头，不需要对外暴露的名字用小写，并且GO语言拥护骆驼命名法，排斥下划线命名法


工具自动生成dockerfile文件

超时时间
3600*time.second

