### nodejs第一课

> https://www.kancloud.cn/kancloud/seven-days-nodejs/43580
>
> 具体的自己下去看一下啊... 时间不多，带你们走一遍简单api，学习更多是靠自己...

#### 什么是node

> JS是脚本语言，脚本语言都需要一个解析器才能运行。对于写在HTML页面里的JS，浏览器充当了解析器的角色。而对于需要独立运行的JS，NodeJS就是一个解析器。
>
> 每一种解析器都是一个运行环境，不但允许JS定义各种数据结构，进行各种计算，还允许JS使用运行环境提供的内置对象和方法做一些事情。例如运行在浏览器中的JS的用途是操作DOM，浏览器就提供了`document`之类的内置对象。而运行在NodeJS中的JS的用途是操作磁盘文件或搭建HTTP服务器，NodeJS就相应提供了`fs`、`http`等内置对象。

#### 作用

> NodeJS让前端众如获神器，终于可以让自己的能力覆盖范围跳出浏览器窗口，更大批的前端工具如雨后春笋。因此，对于前端而言，虽然不是人人都要拿NodeJS写一个服务器程序，但简单可至使用命令交互模式调试JS代码片段，复杂可至编写工具提升工作效率,简而言之就是让前端也能写后端...

#### 安装 

> 自己去看... 时间不多,这个不会我就... https://nodejs.org/en/download/

#### npm

> npm 是一个包管理软件,可以去第三方网站下载自己的包
>
> npm installl .... 

#### 相对路径和绝对路径

> 不必多说吧....

#### nodejs包的加载

> 内置模块(fs,http....),路径...

#### nodejs常用的包和api

* fs
  * fs.readFile(url,encode,callback)
  * fs.readFileSync(url,encode)
  * fs.writeFile(url,data,encode,callback)
  * fs.writeFileSync(url,data,encode)
  * fs.mkdir(url,callback)
  * fs.mkdirSync(url)
  * fs.unLink(url,callback)
  * fs.unLinkSync(url)
  * fs.readdirSync()
  * ....
* http
  * http.createServer(function(req,res){}).listen
  * http.request
  * http.get
  * req.headers
  * req.on("data",function() {})
  * req.on("end",function() {})
* 参数解析 
  * url.parse()
  * querystring.parse()

...剩下的自己下去了解吧，课不多了，node要自己下去学啊，暑假可能会用到哦...

