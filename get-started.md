# 开始

Parse服务的后端搭建很简单，在本书的GitHub仓库中，有我上传的配置好的Parse服务项目，下载下来安装对应的依赖后运行即可。

然后在前端使用Parse的SDK即可与后端完成交互。

## 安装Parse服务



# 集成Parse SDK

集成Parse SDK到你的JavaScript项目中，最简单的方法是通过[npm](https://npmjs.org/parse)安装。

但如果你想使用Parse的预编译文件，你可以从[npm cdn](https://npmcdn.com/)获得。

同时，你可以从[https://npmcdn.com/parse/dist/parse.js](https://npmcdn.com/parse/dist/parse.js) 获得开发版本，从[https://npmcdn.com/parse/dist/parse.min.js ](https://npmcdn.com/parse/dist/parse.min.js)获得压缩后的生产版本。

JavaScript的生态系统非常宽泛，它有着为数众多的框架和运行环境。为了适配各种情况，Parse的npm模块包含了为Node.js和React Native量身定制的SDK版本。最适合的才是最好的，所以，使用合适的npm包，可以确保诸如本地存储、用户会话、HTTP请求之类的项目使用合适的依赖。

在基于浏览器的应用中使用npm包，直接引入：

```js
var Parse = require('parse');
```

在后端应用或Node.js命令行工具中，引入`'parse/node'` ：

```js
// node.js
var Parse = require('parse/node');
```

在React Native应用中，引入`'parse/react-native'` ：

```js
// React Native
var Parse = require('parse/react-native');
```

接下来，用JavaScript初始化你的Parse-Sever，记得替换为你的应用信息：

```js
Parse.initialize("你的appId");
Parse.serverURL = 'http://你的Parse-Server地址:1337/parse'
```

这个JavaScript SDK 最初是基于广受欢迎的Backbone.js框架，它提供了灵活的API，允许你配置你喜欢的JS库。

我们的目标是最小化配置，以便你快速开始构建你的JavaScript和HTML5应用。

目前SDK支持Firefox 23+，Chrome 17+，Safari 5+和IE 10。 IE 9仅支持使用HTTPS托管的应用程序。

