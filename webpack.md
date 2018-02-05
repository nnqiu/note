# webpack

一切皆模块

webpack 有两个环境配置

1. 开发 dev

2. 生产 build

   注: __dirname是nodejs里面的一个全局变量，指向当前执行脚本所在的目录

```
//webpack配置
const webpack = require('webpack')
const HtmlWebpackPlugin = require('html-webpack-plugin');
const ExtractTextPlugin = require('extract-text-webpack-plugin');

module.exports = {
   //报错会找到打包前的位置
   devtool: 'none' ,
   devtool: 'sourmap' ,
   //入口文件
   entry: __dirname + "/app/main.js", //已多次提及的唯一入口文件
   //path.resolve将相对路径转换为绝对路径
   //path.join()连接路径1.unix / 2.windows \
   //出口文件
   output: {
     path: __dirname + "/build",用来存放打包后文件的输出目录
     filename: "bundle-[hash].js",
     publicPath: 指定资源文件引用的目录
   },
   //配置搜索路径的集合 影响webpack模块解析规则 检索
   resolve: {
      root: 配置搜索路径集合 ！！必须是绝对路径
      modulesDirectory: 需要向上搜索的目录名称
      alias：{img: url,echarts: url}
   }
   resolveLoader: {
      auto-import: 
   }
   //前端服务器配置 
   devServer: {
      hot: true,
      contentBase: path.resolve(),
      port: 3000,
      host: '0.0.0.0',
      publicPath: publicPath,
      historyApiFallback: true,
      disabledHostCheck: true
   },
   module: {}
   plugins: {}//数组
}
```

模块

1. 安装

   ```
   全局安装
   npm install -g webpack
   安装到我的项目目录
   npm install --save-dev webpack
   生成package.json
   npm init
   ```

2.  loaders ！！

   将less转化为css es6es7转化为浏览器兼容的js jsx转化为js

   写在modules关键字下进行配置

```
{
  test: /\.jsx?$/,
  exclude: /node_modules/,
  include: /components/,
  use: {
  	loader: 'auto-import',
  	options: {
  		modules: autoImportedModules
  	}
  }
},
```



















