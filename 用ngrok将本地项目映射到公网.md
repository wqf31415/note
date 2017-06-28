### 用 ngrok 将本地 web 项目映射到公网

1. 在本地启动项目，记住项目名和端口号，如我本地项目名为：weichatServer，tomcat启动端口为：8090；

2. 打开命令行工具，切换到 ngrok 目录下，运行以下命令：
```bat
	ngrok -config ngrok.cfg -subdomain weichatServer 8090
```

​	结果如下：
![](http://okbn8yrzu.bkt.clouddn.com/image/ngrok.png "映射结果")

3. 在浏览器中用映射的地址访问，记得要加上项目名：
   http://weichatserver.tunnel.qydev.com/weichatServer/weixin.do

**注意：** 在映射关系中，http://weichatserver.tunnel.qydev.com → 127.0.0.1:8090 ，因此直接输入 http://weichatserver.tunnel.qydev.com 是不行的，会报404错误
