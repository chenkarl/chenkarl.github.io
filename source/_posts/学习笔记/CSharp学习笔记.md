# 特性
C#中通过Type类可以访问任意数据类型信息。
1.获取给定类型的Type引用有3种方式：
  a.使用typeof运算符，如Type t = typeof(int);
  b.使用GetType()方法，如int i;Type t = i.GetType();
  c.使用Type类的静态方法GetType()，如Type t =Type.GetType("System.Double");
2.Type的属性：
  Name：数据类型名；
  FullName：数据类型的完全限定名，包括命名空间；
  Namespace：数据类型的命名空间；
  BaseType：直接基本类型；
  UnderlyingSystemType：映射类型；
3.Type的方法：
  GetMethod()：返回一个方法的信息；
  GetMethods()：返回所有方法的信息。