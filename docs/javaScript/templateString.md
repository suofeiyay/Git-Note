# ES6模板字符串

 模板字符串(Template String)是增强版的字符串，用反引号(`)标识，它可以当作普通字符串使用，也可以用来定义多行字符串，或者在字符串中嵌入变量。 

```javascript
//普通字符串
`This is template string`
//多行字符串
`This is template 
string`
//可以在字符串中嵌入变量
let name="Bob",age=3;
`my name is ${name},my age is ${age}`
//my name is Bob,my age is 3
```

模板字符串的多行字符串，所有的空格和缩进都会保留在输出中。

模板字符串嵌入变量，需要将变量放在'${}'中。

${}中还可以放入表达式，引入对象属性，调用函数，如果直接放入字符串会原样输出。

```javascript
//变量
let name = 'lily',age=12;
`Her name is ${name},her age is ${age}`
//Her name is lily,her age is 12

//对象属性
let obj={
    name:'John',
    score:80
}
`${obj.name},your score is ${obj.score}`
//John,your score is 80

//函数
let func = function(){
    return 'world'
}
`hello ${func}`
//hello world

//字符串
`print this word ${"hi"}`
//print this word hi
```

模拟template string

```javascript
//变量与对象属性
let name = 'lily',age=12;

let str = "my name is ${name},i am ${age}"

let arr = str.split(/\$\{.*?\}/g) //${...}
//arr:["my name is ","i am ",""]

let varr = str.match(/\$\{.*?\}/g)
//varr:["${name}","${age}"]

let outstr = "";
for(let i=0;i<varr.length;i++){
    let s = varr[i].replace('\$\{','').replace('\}','');//"name"
    outstr += arr[i] + eval(s)
}
outstr += arr[arr.length-1]

//name替换为obj.name一样处理
//如果是函数，eval(s+'()');需要添加'()'执行函数

```

注：

 eval() 函数接受原始字符串作为参数，如果参数不是原始字符串，该方法不做任何改变的返回。 

```javascript
eval({obj:1}) //{obj:1}
```

如果传入的参数是变量名，执行后返回变量名对应的变量值。

```javascript
let a="hi"; eval('a') // "hi"
```

如果传入的参数为函数名，执行时会执行对应的函数，并返回函数的返回值

```javascript
let fuc= function(){
    console.log('1')
    return 'hi'
}
eval("fuc")
//执行函数 打印 '1'
//返回值 hi
```



参考链接：https://github.com/ruanyf/es6tutorial/blob/f9e16e462df103b8df30f7c7ce742a3b0898c9b4/docs/string.md

https://www.w3school.com.cn/js/jsref_eval.asp