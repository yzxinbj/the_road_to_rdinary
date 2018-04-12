# smarty环境搭建

## 背景
前端利用node模拟后端web服务，利用mock假数据来实现前后端分离  
windows下启动基于node的edp服务，调用php来渲染smarty模板

## 问题及原因
edp webserver服务启动后渲染smarty模板报错：
```
on line 57 &quot;{%$len = mb_strlen($info.user.name, 'utf-8')%}&quot; 
unknown function &quot;mb_strlen&quot;'
```
由新安装的php未打开mb拓展造成

## 解决办法
打开mb拓展：
- 在php目录下找到php.ini（没有的话复制php.ini-development为php.ini）
- 修改此文件中的语句，去掉分号，并更改`extension_dir`为你本机的php目录

```
;extension_dir = "./"        ==变成==>  extension_dir = "/php"(你自己的php目录地址)
;extension_dir = "ext"       ==变成==>  extension_dir = "ext"
;extension=php_mbstring.dll  ==变成==>  extension=php_mbstring.dll

```
## 报 php-cgi 错误
安装 php 时 追加 --with-cgi 参数，或改装 php56