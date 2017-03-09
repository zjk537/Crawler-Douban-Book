# Crawler-Douban-Book
使用NodeJs+express+MongoDB实现的简单爬虫系统，用来爬取豆瓣读书的书籍数据，并保存进MongoDB数据库。

## 通过本项目能学到什么？

通过本项目能够学到以下知识。
+ 基本的爬虫系统怎么实现。
+ request请求获取页面后怎么处理
+ express的基本使用和路由的使用。
+ 怎么用log4js来记录日志信息。
+ node中怎么操作mongoDB数据库。
+ 基本的MVC架构操作数据（其实没有View层）。
+ 使用mongolass对数据库进行增删改查。


## 环境

NodeJs：`6.10.0`

express：`4.15.2`

mongoDB：`3.4.2`

## 插件

cheerio：`0.22.0`

主要用来生成DOM树，方便操作页面。

log4js：`1.1.1`

主要用来代替express的默认日志系统，用来记录日志。

mongolass：`2.4.2`

用来连接mongoDB数据库的驱动。

request：`2.80.0`

用来发送请求，获取页面内容。

## 其他插件
下列插件为开发测试使用，推荐安装。

node-dev：`3.1.3`

用来测试自动重启服务，方便修改代码后及时测试。相应的也可以使用supervisor、nodemon等插件代替。
## Dev
**下载项目**

> git clone https://github.com/BingKui/Crawler-Douban-Book.git

**进入目录安装相应依赖**

> cd Crawler-Douban-Book && npm install

**修改配置**

修改项目配置项，打开config目录下的config.js文件，修改数据库连接的配置和端口。

修改下列的数据库地址为自己的数据库地址
> mongodb://localhost/splider

**运行项目**

>npm run start

注意：如果没有安装`node-dev`需要修改`package.json`中的`script`。

**测试效果**

打开浏览器，或者请求发送工具（如：[Postman](https://www.getpostman.com/)），打开`http://localhost:3000/tag`获取标签相应的数据，并保存进mongoDB数据库。

## 路由说明

`http://localhost:3000/tag`：获取标签，并保存进数据库。

`http://localhost:3000/tag/update`：获取每个标签的页码总数，并对数据库中的数据进行更新。

`http://localhost:3000/tagList`：获取每个标签包含的所有书籍数据，并保存进数据库。

待后续添...

## 更新日志
[更新日志](./docs/update.md)