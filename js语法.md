

# 基础js语法

### 对象

`var person = {
    firstName: "John",
    lastName : "Doe",
    id : 5566,
    fullName : function() 
	{
       return this.firstName + " " + this.lastName;
    }
};
document.getElementById("demo").innerHTML = person.fullName();`

对象中的属性方法调用，不加入括号会返回函数的定义

### 返回值

`function myFunction(a,b) {    return a*b; }  document.getElementById("demo").innerHTML=myFunction(4,3);`

### 事件

| onchange    | HTML 元素改变                        |
| ----------- | ------------------------------------ |
| onclick     | 用户点击 HTML 元素                   |
| onmouseover | 鼠标指针移动到指定的元素上时发生     |
| onmouseout  | 用户从一个 HTML 元素上移开鼠标时发生 |
| onkeydown   | 用户按下键盘按键                     |
| onload      | 浏览器已完成页面的加载               |

### 字符串以及字符串方法

[JavaScript 字符串 | 菜鸟教程 (runoob.com)](https://www.runoob.com/js/js-strings.html)

### 运算符

| +     | 加法         | x=y+2 | 7                                                            | 5    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_add) |
| ----- | ------------ | ----- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| -     | 减法         | x=y-2 | 3                                                            | 5    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_sub) |
| *     | 乘法         | x=y*2 | 10                                                           | 5    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_mult) |
| /     | 除法         | x=y/2 | 2.5                                                          | 5    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_div) |
| %     | 取模（余数） | x=y%2 | 1                                                            | 5    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_mod) |
| ++    | 自增         | x=++y | 6                                                            | 6    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_incr) |
| x=y++ | 5            | 6     | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_incr2) |      |                                                              |
| --    | 自减         | x=--y | 4                                                            | 4    | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_decr) |
| x=y-- | 5            | 4     |                                                              |      |                                                              |

| =    | x=y  |       | x=5  | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_equal) |
| ---- | ---- | ----- | ---- | ------------------------------------------------------------ |
| +=   | x+=y | x=x+y | x=15 | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_plusequal) |
| -=   | x-=y | x=x-y | x=5  | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_minequal) |
| *=   | x*=y | x=x*y | x=50 | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_multequal) |
| /=   | x/=y | x=x/y | x=2  | [实例 »](https://www.runoob.com/try/try.php?filename=tryjs_oper_divequal) |
| %=   | x%=y | x=x%y | x=0  |                                                              |

| 运算符 | 描述 | 例子                      |
| :----- | :--- | :------------------------ |
| &&     | and  | (x < 10 && y > 1) 为 true |
| \|\|   | or   | (x==5 \|\| y==5) 为 false |
| !      | not  | !(x==y) 为 true           |

### 语句

if (time<20) {    x="Good day"; }

`if (time<10) `

 `{    document.write("<b>早上好</b>"); } `

`else if (time>=10 && time<20)`

 ` {    document.write("<b>今天好</b>"); } `

`else {    document.write("<b>晚上好!</b>");`





`var d=new Date().getDay(); `

`switch (d)`

` {    case 6:x="今天是星期六";   ` 

` break;   ` 

​    ` case 0:x="今天是星期日";    ` 

`break;    `

`default:    x="期待周末"; }` 

` document.getElementById("demo").innerHTML=x;`





```
var i=0,len=cars.length;
for (; i<len; )
{ 
    document.write(cars[i] + "<br>");
    i++;
}
```

```
var person={fname:"Bill",lname:"Gates",age:56}; 
 
for (x in person)  // x 为属性名
{
    txt=txt + person[x];
}
```

```
cars=["BMW","Volvo","Saab","Ford"];
var i=0;
while (cars[i])
{
    document.write(cars[i] + "<br>");
    i++;
}
```

### break

```
cars=["BMW","Volvo","Saab","Ford"];
list: 
{
    document.write(cars[0] + "<br>"); 
    document.write(cars[1] + "<br>"); 
    document.write(cars[2] + "<br>"); 
    break list;
    document.write(cars[3] + "<br>"); 
    document.write(cars[4] + "<br>"); 
    document.write(cars[5] + "<br>"); 
}
```

### 正则

```
https://www.runoob.com/js/js-regexp.html
```





### 错误捕捉

```
var txt=""; 
function message() 
{ 
    try { 
        adddlert("Welcome guest!"); 
    } catch(err) { 
        txt="本页有一个错误。\n\n"; 
        txt+="错误描述：" + err.message + "\n\n"; 
        txt+="点击确定继续。\n\n"; 
        alert(txt); 
    } 
}
```

### 表单

```
function validateForm() {
    var x = document.forms["myForm"]["fname"].value;
    if (x == null || x == "") {
        alert("需要输入名字。");
        return false;
    }
}

function validateForm()
{
  var x=document.forms["myForm"]["fname"].value;
  if (x==null || x=="")
  {
    alert("姓必须填写");
    return false;
  }
}
```

### 验证api

[HTML5 Input 类型 | 菜鸟教程 (runoob.com)](https://www.runoob.com/html/html5-form-input-types.html)





### this

| disabled  | 规定输入字段是禁用的       |
| --------- | -------------------------- |
| max       | 规定允许的最大值           |
| maxlength | 规定输入字段的最大字符长度 |
| min       | 规定允许的最小值           |
| pattern   | 规定用于验证输入字段的模式 |
| readonly  | 规定输入字段的值无法修改   |
| required  | 规定输入字段的值是必需的   |
| size      | 规定输入字段中的可见字符数 |
| step      | 规定输入字段的合法数字间隔 |
| value     | 规定输入字段的默认值       |

```


var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```







### let

```
let x = 2;       // 合法
var x = 3;       // 不合法

{
    let x = 4;   // 合法
    var x = 5;   // 不合法
}
let 关键字在不同作用域，或不同块级作用域中是可以重新声明赋值的:

let x = 2;       // 合法

{
    let x = 3;   // 合法
}

{
    let x = 4;   // 合法
}
```







### json

```
var text = '{ "sites" : [' +
    '{ "name":"Runoob" , "url":"www.runoob.com" },' +
    '{ "name":"Google" , "url":"www.google.com" },' +
    '{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
    
obj = JSON.parse(text);
document.getElementById("demo").innerHTML = obj.sites[1].name + " " + obj.sites[1].url;
```









### 异步编程

```
setTimeout(function () {
    document.getElementById("demo1").innerHTML="RUNOOB-1!";
}, 3000);
document.getElementById("demo2").innerHTML="RUNOOB-2!";
console.log("2");
```







```
new Promise(function (resolve, reject) {
    setTimeout(function () {
        console.log("First");
        resolve();
    }, 1000);
}).then(function () {
    return new Promise(function (resolve, reject) {
        setTimeout(function () {
            console.log("Second");
            resolve();
        }, 4000);
    });
}).then(function () {
    setTimeout(function () {
        console.log("Third");
    }, 3000);
});
```

