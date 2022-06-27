# 项目创建
创建一个基于"webpack"模板的新项目,项目名称可自定义,这里用默认的"my-project"
cmd或者git bash输入`vue init webpack my-project`
接下来会出现
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1iN2M3MTBkMzEwMTg5NDA3LnBuZw)
这里直接回车默认就是my-peoject

然后下图是是项目描述,不是必填,按下回车继续
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny0xMDYwNTI3ZWU3NmMzYzAyLnBuZw)
然后是项目作者
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1lODJmMzI5Y2M5MWYwZWQ4LnBuZw)
然后需要选择是否安装编译器
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny0yZTE1ZmVkNzIxN2E2MmQ0LnBuZw)

安装要选择Vue build方式时有两种:
standaloe方式打包的是/node_modules/vue/dist/vue.common.js
runtime打包的是/node_modules/vue/dist/vue.js
这两种方式对普通用户来说差不多,选一个大多数用的就可以了,然后按下Enter键

然后是否安装路由
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny00YmVhZmQ1ZjlkMDE1YzRlLnBuZw)

是否使用ESLint,它是一个按照ECMAScript并且按照规则给出爆的代码检测工具,它可以避免低级错误并统一代码风格,但是需要严格按照规范来写,按自己习惯来,本文这里选n,然后回车
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1lMWE1NzUxODI5OTU0YzRiLnBuZw)
接着是否安装单元测试工具,可根据开发需求,本文这里选n然后回车
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny0xYmU3ZTYxZWJhZDc5MGFiLnBuZw)
接着是否安装e2e测试工具,可根据开发需求,本文这里选择n
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1jYjE2Y2YwOTZjMTgwMGI4LnBuZw)
然后是项目创建后是否直接使用命令安装依赖包?
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1iMzc3YzIwZjYwMjc4MWU1LnBuZw)
第一个:是的,使用npm安装,
第二个:是的,使用Yarm命令安装
第三个:不,自己手动安装
这里本文直接回车选第一个
然后到出现以下界面就可以了
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1iNzZhNzAxYzVkMTMwNzVkLnBuZw)
然后进入根目录
`cd my-project`
安装依赖
`cnpm install`
然后会在根目录下发现多了个node_modules文件夹,就是安装的依赖文件夹
![image.png](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1lYzE4YTIzNmUzOGYzNzYxLnBuZw)
然后运行项目,输入`npm run dev`,出现http://localhost:8080并在浏览器访问即可
***
# 注意事项:
有时会出现安装后8080端被占用无法访问的情况(如运行了腾讯QQ),可以手动解除:
在命令行中输入netstat -ano，列出所有端口的情况。在列表中我们观察被占用的端口，这里是找到占用的8080，

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny0wM2JiNDVkNTU4MzkxYzBmLmpwZw)

2、查看被占用端口对应的PID，即，后面的2724，若觉得有点多，不太好找的话，

输入命令：netstat -aon|findstr "8080" （这里以8080端口为例），回车，记下最后一位数字，即PID,这里是2724。

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny1mNWMzNjk0NGVhZjQ4NDVmLmpwZw)

3、继续输入tasklist|findstr "2724"，回车，查看是哪个进程或者程序占用了端口，结果是：node.exe

4、在cmd的命令窗口中输入：taskkill /f /t /im node.exe，即可，结束进程，解除占用的端口。

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly91cGxvYWQtaW1hZ2VzLmppYW5zaHUuaW8vdXBsb2FkX2ltYWdlcy8xODMwMzA3Ny0xNGVkN2E2NjUyNTJlMWFjLmpwZw)
解除占用后,得重新运行启动一次,用ctrl+c停掉之前运行的`npm run dev`,再用`npm run dev`运行一次即可,若仍然得不到解决,可以试着重启计算机,正常来说在qq前运行`npm run dev`是不会被占用的
***
如果本文帮助到你了,请点赞收藏,谢谢支持
简书同步文章https://www.jianshu.com/p/3c39f4d9778d