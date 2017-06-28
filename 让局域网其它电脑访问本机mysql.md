### 设置让局域网其它电脑可以连接本机 MySql 数据库

- 打开命令行，用 root 账号登录；

- 依次执行以下指令：

```mysql
	GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456' WITH GRANT OPTION;
	-- 其中百分号 **%** 为通配符，表示任何ip可连接，可以换成指定 ip 
	-- **123456** 为连接密码
```
```mysql
	flush privileges;
```