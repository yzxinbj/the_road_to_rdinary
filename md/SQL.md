# SQL
> 大小写不敏感  
> 分号是在数据库系统中分隔每条 SQL 语句的标准方法，  
> 这样就可以在对服务器的相同请求中执行一条以上的 SQL 语句。
```
DISTINCT: 不同
ALTER: 改变、变更
descend:  降落
ascend： 上升

```

## 一些重要的 SQL 命令

SELECT - 从数据库中提取数据  

UPDATE - 更新数据库中的数据  

DELETE - 从数据库中删除数据  

INSERT INTO - 向数据库中插入新数据  

CREATE DATABASE - 创建新数据库  

ALTER DATABASE - 修改数据库  

CREATE TABLE - 创建新表  

ALTER TABLE - 变更（改变）数据库表  

DROP TABLE - 删除表  

CREATE INDEX - 创建索引（搜索键）  

DROP INDEX - 删除索引  



## 少废话看例子

```text
"Websites" 表的数据
+----+--------------+---------------------------+-------+---------+
| id | name         | url                       | alexa | country |
+----+--------------+---------------------------+-------+---------+
| 1  | Google       | https://www.google.cm/    | 1     | USA     |
| 2  | 淘宝          | https://www.taobao.com/   | 13    | CN      |
| 3  | 菜鸟教程      | http://www.runoob.com/    | 4689  | CN      |
| 4  | 微博          | http://weibo.com/         | 20    | CN      |
| 5  | Facebook     | https://www.facebook.com/ | 3     | USA     |
+----+--------------+---------------------------+-------+---------+
```



## 1、
use RUNOOB; 命令用于选择数据库。 
 
set names utf8; 命令用于设置使用的字符集。  

SELECT name,country FROM Websites;  
从 "Websites" 表中选取 "name" 和 "country" 列

SELECT DISTINCT country FROM Websites;  
从 "Websites" 表的 "country" 列中选取唯一不同的值，也就是去掉 "country" 列重复值

## 2、WHERE 子句
> SQL使用单引号来环绕文本值（大部分数据库系统也接受双引号）。  
> 在上个实例中 'CN' 文本字段使用了单引号。  
> 如果是数值字段，请不要使用引号。  

### WHERE 子句中的运算符
> <> : 不等于。注释：在`SQL`的一些版本中，该操作符可被写成 !=  
> BETWEEN : 在某个范围内   
> LIKE : 搜索某种模式  
> IN : 指定针对某个列的多个可能值  
> AND : 且  
> OR : 或  


### where 例子
SELECT * FROM Websites WHERE country='CN';  
从 "Websites" 表中选取国家为 "CN" 的所有网站

SELECT * FROM Websites
WHERE alexa > 15
AND (country='CN' OR country='USA');  
从 "Websites" 表中选取 alexa 排名大于 "15" 且国家为 "CN" 或 "USA" 的所有网站

## 3、ORDER BY 关键字
ASC|DESC : 升序或降序

SELECT * FROM Websites ORDER BY alexa DESC;   
从 "Websites" 表中选取所有网站，并按照 "alexa" 列降序排序

SELECT * FROM Websites ORDER BY country,alexa;  
从 "Websites" 表中选取所有网站，并按照 "country" 和 "alexa" 列排序，先按country排，再按alexa排
 
## 4、INSERT INTO 语句







