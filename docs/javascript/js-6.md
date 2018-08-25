# 如何让Nodejs支持对应的ES
  &emsp;&emsp;不同版本的Node.js对Babel有不同的支持，如若是Nodejs支持ES6语法，需要引入babel。因此要安装一些babel的依赖包，如babel-preset-es2015 / babel-core /babel-cli。  
  &emsp;&emsp;ES6对应es2015，ES7对应es2016，ES8对应es2017，同时对应支持的node版本更高  

 #### 检测ES6
 
可以使用es-checker来检测当前Node.js对ES6的支持情况，全局安装es-checker  

  ```js
$ npm install -g es-checker
  ```
  
安装好之后，执行以下命令来查看Node.js对ES6的支持情况:  
  ```js
  $ es-checker
  ```
可以从输出中查看当前版本Node.js(v7.7.4)对ES6的支持情况

 #### 添加es6支持
全局安装babel-cli， 项目安装 babel-preset-es2015: 

  ```js
npm install babel-cli -g
npm install babel-preset-es2015 --save
  ```
安装完之后，还需要添加一个名为.babelrc的配置文件。方便babel-cli使用babel-preset-es2015。文件内容如下：  
  ```js
{
  "presets": ["es2015"],
  "plugins": [
    "add-module-exports"
  ]
}
  ```
 或者在项目入口文件（如app.js）引用下babel:   
   ```js 
  require(‘babel-register‘)({
    presets: [‘es2015‘]
}); 
  ```
  

 