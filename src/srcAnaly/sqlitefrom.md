# SQLite中FROM子句的使用
FROM后跟一个或多个表名，也能跟一个虚表或者一个子程序的查询结果集。如果源表只有一个，那就是直接使用，如果是两个或多个，一般使用内连接或者外连接。采用连接的方式，就不是简单的用逗号把表名隔开。<br>
在SQLite中，FROM子句是一棵语法树，用表达式列表SrcList（结构体）来表示，表之间的连接用sqliteProcessJoin()函数处理。最基础的处理策略是嵌套查询。
