# meta标签

[TOC]

#### 1.meta标签

```html
<meta charset="UTF-8">
```

 meta常用于定义页面的说明，关键字，最后修改日期，和其它的元数据。这些元数据将服务于浏览器（如何布局或重载页面），搜索引擎和其它网络服务。 

##### 1.1类型

​	常用的就是 charset , name , http-equiv

##### 1.2 charset

代表字符集声明，告诉文档使用哪种字符编码

这个属性值必是和ASCII大小写无关的"utf-8"

```html
<meta charset="UTF-8">
```

##### 1.3 name

name 和 content 属性可以一起使用，以名-值对的方式提供元数据。

常用的name值有:

###### 1.3.1. keywords（关键字）

用于告诉搜索引擎，网页的关键字

```html
<meta name="keywords" content="官网,前端">
```

###### 1.3.2 description（网站内容的描述）

用于告诉搜索引擎，网站的主要内容

```html
<meta name="description" content="网站主要内容是...">
```

###### 1.3.3 viewport 

用于手机设备，规定视图

width：可以设置为具体数值，也可以设置为 device-width 

height：可以设置为具体数值，也可以设置为device-height

initial-scale：0.0-10.0之间的数值，代表初始缩放值

maximum-scale：0.0-10.0之间的数值，代表最大缩放值（ iOS10+  忽略）

minimum-scale：0。0-10.0之间的数值，代表最小缩放值（ iOS10+  忽略）

user-scalable：yes 或 no，用户是否能够缩放（ iOS10+  忽略）

移动端常用设置：

```html
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no"/>
```

###### 1.3.4 author（作者）

```html
<meta name="author" content="作者是一个热爱前端的人">
```

###### 1.3.5 referrer

控制从文档发出的http请求的Referer首部的内容，content内容有

no-referrer：不发送http Referer首部

origin：发送当前文档的origin

no-referrer-when-downgrade：默认行为

origin-when-crossorigin：同源请求下，发送完整url(不含参数)，其他情况下发送origin

unsafe-URL:同源请求下，发送完整url(不含参数)

动态插入不起作用，多个策略冲突是，no-referrer生效

###### 1.3.6  robots （爬虫）

```html
<meta name="robots" content="all|none|index|noindexx|follow|nofollow">
```

none : 搜索引擎将忽略此网页，等价于noindex，nofollow
noindex : 搜索引擎不索引此网页
nofollow: 搜索引擎不继续通过此网页的链接索引搜索其它的网页
all : 搜索引擎将索引此网页与继续通过此网页的链接索引，等价于index，follow
index : 搜索引擎索引此网页
follow : 搜索引擎继续通过此网页的链接索引搜索其它的网页 

###### 1.3.7 copyright （版权）

```html
<meta name="copyright" content="版权所有归属"
```

##### 1.4 http-equiv

定义了一个编译指示指令，所允许的值都是特定HTTP头部的名称

###### 1.4.1 content-security-policy

定义当前页的内容策略，有助于防止跨站点脚本攻击，设置白名单制度，详细解析可以参考[链接](http://www.ruanyifeng.com/blog/2016/09/csp.html) 

###### 1.4.2  content-type 

 设定网页字符集，便于浏览器解析与渲染页面 ，可以用charset设置

###### 1.4.3  cache-control(指定请求和响应遵循的缓存机制)

浏览器如何缓存响应以及缓存多长时间

```html
<meta http-equiv="cache-control" content="no-cache">
```

no-cache: 先发送请求，与服务器确认该资源是否被更改，如果未被更改，则使用缓存
no-store: 不允许缓存，每次都要去服务器上，下载完整的响应
public : 缓存所有响应，但并非必须。因为max-age也可以做到相同效果
private : 只为单个用户缓存，因此不允许任何中继进行缓存
maxage : 表示当前请求开始，该响应在多久内能被缓存和重用，而不去服务器重新请求。例如：max-age=60表示响应可以再缓存和重用 60 秒。

```html
<meta http-equiv="cache-control" content="no-siteapp">
```

no-siteapp：禁止百度自动转码 

###### 1.4.4 expires(网页到期时间)

```html
<meta http-equiv="expires" content="Wed, 21 Oct 2015 07:28:00 GMT">
```

###### 1.4.5  refresh （自动刷新并指向某页面）

```html
<meta http-equiv="refresh" content="2; URL=http://www.baidu.com/">
```

自动刷新，2秒后，自动跳转百度，去掉URL则只是刷新当前页面，可做页面跳转（重定向）

###### 1.4.6  X-UA-Compatible：浏览器采取何种版本渲染当前页面 

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
```

指定IE和Chrome使用最新版本渲染当前页面

###### 1.4.7  Set-Cookie：为页面定义cookie 

```html
<meta http-equiv="Set-Cookie" content="name,date">
<meta http-equiv="Set-Cookie" content="User=Lxxyx; path=/; expires=Sunday, 10-Jan-16 10:00:00 GMT"> //具体范例
```

参考链接：

https://segmentfault.com/a/1190000004279791

https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta