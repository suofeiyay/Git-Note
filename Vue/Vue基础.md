# Vue基础

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

