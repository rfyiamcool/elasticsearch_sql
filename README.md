# elasticsearch_sql

其实原本是想用ast自定义语法树来实现的,结果琢磨了一晚上,还是自己写个简单的解释器吧. AST解析SQL语句实在有些复杂.

下面实现的用法:  

select * from index.type;

select keyword from index.type;

select keyword from index.type where keyword = '宝马';

select keyword from index.type where keyword = '宝马' and id = '88';

select keyword from index.type where keyword = '宝马' and id = '88' order by id DESC;

select count(id) from index.type where keyword = '宝马' and id = '88' order by id DESC;

select avg(price) from index.type where keyword = '宝马' and id = '88' order by id DESC;

select avg(price) from index.type where keyword = '宝马' and id = '88' and cdate between '2015-10-10' and '2015-10-15' ;



