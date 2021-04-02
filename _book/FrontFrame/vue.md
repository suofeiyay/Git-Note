# vue

#### *引用方式

script标签引用

npm包安装

npm install -g vue-cli

实例化项目

vue init webpack

启动项目

npm run dev 

打包项目

npm run build

vue-cli3安装

卸载老版本vue-cli：   npm  uninstall vue-cli -g

安装新版本：  npm install -g @vue/cli

原型开发：  npm install -g @vue/cli-service-global 

创建项目： vue create project-name

使用图形化界面：vue ui 



错误提示：

安装3.0 提示“Unexpected end of JSON input while parsing near···”

解决办法：
npm cache clean --force
npm cache verify
npm i -g @vue/cli

查看版本：vue -V

nvm可以在本地搭建不同版本的node.js

vscode alt+b在浏览器打开





vue官网 https://cn.vuejs.org/v2/guide/ 

#### *辅助开发工具

vue-devtools，安装在google，辅助调试Vue

https://github.com/vuejs/vue-devtools#vue-devtools

## 1.原理

​	双向绑定：基于ES5的object.defineProperty()重新定义对象的set方法(对象设置属性值)和get方法（获取属性值）

object.defineProperty(参数1，参数2，参数3)返回该对象的obj

参数1：传入对象obj1

参数2：要定义或修改的属性名

参数3：属性描述符（数据描述符，存取描述符，{}）