---
title: SQL数据库
date: 2020-04-18 15:22:38
tags:
<font size='2'>标签：服务器可能资源不足，或者不信任该程序集</font>
---
##程序运行可能会遇到信任问题
#####错误内容：<br/>
<p> &nbsp; &nbsp; &nbsp; &nbsp 错误编号:yieldmanage_yieldtransitedit_aspx,10
System.Data.SqlClient.SqlException: 在尝试加载程序集 ID 65670 时 Microsoft .NET Framework 出错。
<font face="微软雅黑" color="red" >服务器可能资源不足，或者不信任该程序集，因为它的 PERMISSION_SET 设置为 EXTERNAL_ACCESS 或 UNSAFE。</font>请重新运行查询，或检查有关的文档了解如何解决程序集信任问题。有关此错误的详细信息: System.IO.FileLoadException: 
未能加载文件或程序集“updatestate, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null”或它的某一个依赖项。
发生与安全有关的错误。</p>

#####解决方法:

<p>
--启用’clr enabled‘报错(尝试加载程序集时失败)<br/>
--信任改为true<br/>
--打开信任<br/>
ALTER DATABASE [Test20190729]  SET TRUSTWORTHY ON<br/>
go<br/>
--设置数据库所有者<br/>
ALTER AUTHORIZATION ON database::[Test20190729] TO sa<br/>
--开启clr功能<br/>
exec sp_configure 'clr enabled', 1;<br/>
reconfigure;<br/>


</p>

**注意：[Test20190729]为数据库名称。**