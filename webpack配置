## webpack配置

### 1.初始化项目

- npm init

### 2.安装webpack webpcak-dev-server

- yarn add webpack -g
- yarn add webpack-dev-server --save-dev

### 3.配置package.json

```json
"script":{
    "start": "webpack-dev-server --open --inline",
    "build": webpack --config webpack.config.js
}
```

### 4.创建webpack配置文件

- 在项目根目录创建webpack.config.js

### 5.配置webpack.config.js

- ```javascript
  module.exports= {
      mode: 'development', // webpack打包的模式 development为开发模式，productions为正式版打包文件
      entry：path.join(__dirname,'/src/index.js'), // 入口文件(可以多文件，详情看官方文档)
      output: {
         path: path.join(__dirname,'/dist'), // 打包文件的路径
         filename: 'bundle.js' // 打包文件的名字
      },
      module: {
          rules: [
              {
                  test: /\.js$/,  // 要处理的文件类型,
                  exclude: /node_modules/,
                  use: {
                      loader: 'babel-loader' // 要使用的loader
                  }
              }
          ]
      }，
      plugins:[
          new HtmlWebpackPlugin({ // 个人理解: 为单页面应用创建一个入口html文件以及引入script和link css，多页面应用请自行查询
              template: './src/index.html', // 要输出的模板html文件
              filename: 'index.html' // 输出的文件名
          })
      ]，
      devServer: { //本地服务器的配置:webpack-dev-server会为我们创建一个本地服务器（个人理解）
          port: 3000， //端口号
      }
  }
  ```

### 6.安装各项依赖 如：babel-loader

- babel-loader 7.0.0版本以上请使用
  - @babel/core
  - @babel/plugin-proposal-class-properties
  - @babel/preset-env
  - @babel/preset-react

### 7.项目根目录创建.babelrc配置文件

- ```json
  {
      "presets": [ // 预置
          "@babel/preset-env",
          "@babel/react"
      ],
      "plugins": [ // 插件
          "@babel/plugin-proposal-class-properties" // 支持class对象写法
      ]
  }
  ```

### 8.运行npm start启动项目

- 到此 基本的配置已完成，按照项目的需要添加配置 如：less/sass等

