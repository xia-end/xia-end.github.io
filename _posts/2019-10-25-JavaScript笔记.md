[TOC]
# JavaScript笔记

## 认识什么是js
>js是JavaScript的简称
## 作用区分
>html:呈现网页的内容
>css:用于设置网页的样式
>js:设置网页的特效

## js的作用
>1. 用于校验用户输入的表单数据
>2. 用于与用户进行交互式体验
>3. Ajax异步加载技术
>4. 实现瀑布流,无刷新加载数据

## 在HTML中使用js的方式
>1. 直接在head标签中定义script标签来定义js
>2.可以在Html标签中直接使用js事件属性设置js
>3. 使用script标签引用外部的js文件
>4. 在超链接href属性中使用JavaScript标识符定义js
>  例:
>
>  ```javascript
>  <script>
>  </script>
>  ```
>
>  

## JavaScript的注释
>ps:推荐将script标签写在body标签的外面
>//:单行注释
>/**/:多行注释
>/**:文档注释
>*/

## js的指令的分割符
>指令分隔符,用于标志我们所写的代码结束(一行语句的结束)
>1. 使用分号作为指令分隔符(推荐)
>2.使用换行符作为指令分隔符

## js的内容
> js的内容:
>     客户端的浏览器的js
>     1.ECMAScript的核心语法结构(如何使用js,如何定义js的变量)
>     2.包含DOM对象
>     3.包含BOM对象

## js的变量
>变量:存储值的容器
>声明一个变量,后续方便使用和计算
>### js中声明变量
>格式:var 变量名 = 值; 
>变量的类型:
>>Number:数值类型
>>Boolean:布尔类型
>>String:字符串类型
>>Function:函数类型
>>Object:对象类型
>>Undefined:未定义
>### 变量的命名规则
>>首字母必须是字母,下划线,$
>>后跟任意长度的数字,字母,下划线,$
>>严格区分大小写
>>不允许使用js的关键字和保留字
>>1.关键字:js已经使用的字
>>2.保留字:系统打算去用,但是目前没有使用
>### 数值型:
>1.数值型
>2.小数(浮点型)
>3.NaN:一个不是数字的数值类型
>>1.应该返回一个数字结果,但是回发不了,此时返回NaN
>>特点:
>>>a.NaN与任何一个数字进行运算返回的结果都是NaN
>>>b.NaN不与任何一个数相等  
>### 强制类型转换
>>使用Number()函数将其他类型变量转换为数值类型
>>>1.数值类型以原样输出
>>>2.布尔值
>>>true 转为1
>>>false 转为0
>>>3.字符串类型
>>>空字符串转为数值类型 0
>>>字符串是符合结构的数值返回对应的数值
>>>只要有非数字字符(除了第一个小数点以外的字符)转为NaN;
>>>4.未定义类型转为NaN

>>使用parsInt()将其他类型的变量尝试转化为数值类型的整数
>>>1.数值类型
>>>
>>>>整数 原样输出
>>>>小数 去除小数的位数,保留整数
>>>>2.布尔值类型全部转换为NaN
>>>>3.字符串类型
>>>>空格字符串转换为数值类型 0
>>>>首字母是否是数值类型:
>>>>>不是:直接转换为NaN
>>>>>是:只识别对应的有效的整数
>>>>
>>>>4. undefined 转换为NaN

>>其他类型变量转换为布尔值为假的情况:
>>>1.布尔类型的将
>>>2.数值类型
>>>>0/0.0/NaN
>>>3.未定义类型 Undefined
>>>字符串类型的 空字符串 ''

## js的运算符
>变量是存储值得容器
>将变量进行相关的数学运算.逻辑运算等其他运算的符号
>### 运算符的种类:
>>算术运算符:
>>>+,-,*,/
>>赋值运算符:
>>>=
>>比较运算符
>>> 大于小于
>>连接运算符
>>> +
>>> 逻辑运算符
>>> 逻辑与 逻辑或 逻辑

## JavaScript的输出
>### JavaScript显示数据
>JavaScript可以通过不同的方式来输出数据
>1.widow.alert();或alert():弹出警告框
>2.document.write():将内容写到html文件中
>3.innerHTML:将内容写入到HTML元素
>4.使用console.log():将内容写入到控制台

## JavaScript的语句 
>### JavaScript 语句标识符
>>|语句|描述|
>>|:----|:----|
>>|break|用于跳出循环|
>>|catch|语句块,在try语句块执行出错时执行catch语句块|
>>|continue|跳出循环中的一个迭代|
>>|do...while|执行一个语句块,在条件语句为true是继续执行该语句块|
>>|for|用于跳出循环|
>>|for...in|用于遍历数组或对象的属性(对数组或者对象的属性进行循环操作)|
>>|function|定义一个函数|
>>|if...else|用于基于不同的条件来执行不同的动作|
>>|return|退出函数|
>>|switch|用于基于不同的条件执行不同的动作|
>>|try|实现错误处理,与catch一同使用|
>>|var|声明一个变量|
>>|while|当条件语句为true时,执行语句块|

## JavaScript的数组
>下面代码创建名为cars的数组
>
>```javascript
>var cars=new Array();
>cars[0]="Saab";
>cars[1]="Volvo";
>cars[2]="BMW";
>```
>
>或者(condensed array):
>
>```javascript
>var cars=new Array("Saab","Volvo","BMW");
>```
>
>或者(literal array):
>
>```javascript
>var cars=["Saab","Volvo","BMW"];
>```

## JavaScript对象
>对象由花括号分隔.在括号内部,对象的属性以名称和键值对的形式(name:value)来定义.属性由逗号分隔:
>示例:
>
>```javascript
>var person={firstname:"John",lastname:"Doe",id:5566};
>```
>
>声明可跨多行:
>
>```javascript
>var person={
>firstname : "John",
>lastname : "Doe",
>id                 : 5566
>};
>```

## 声明变量类型
>当声明新变量时,可以使用关键词"new"来声明其类型:
>
>```javascript
>var carname=new String;
>var x=      new Number;
>var y=      new Boolean;
>var cars=   new Array;
>var person= new Object;
>```
>JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。

## js事件
### JavaScript事件
>HTML事件是发生在HTML元素上的事情
>当在HTML页面中使用JavaScript时,JavaScript可以触发这些事件

### HTML事件   
>HTML事件可以是浏览器行为,也可以是用户行为.
>以下是HTML事件实例:
>>1.HTML 页面完成加载
>>2.HTML input字段改变时
>>3.HTML 按钮被点击

### 常见的HTML事件
>TML常见的事件列表:
>|事件|描述|
>|:----|:----|
>|onchange|HTML元素改变|
>|onclick|用户单击HTML元素|
>|onmouseover|用户在一个HTML元素上移动鼠标|
>|onmouseout|用户从一个HTML元素上移开鼠标|
>|onkeydown|用户按下键盘按键|
>|onload|浏览器|

### JavaScript的用途
>### 用于处理表单验证,用户输入,用户行为及浏览器动作:
>>1.页面加载时触发事件
>>2.页面关闭时触发事件
>>3.用户点击按钮执行动作
>>4.验证用户输入内容的合法性
>>等等... 
>### 可以使用多种方法来执行JavaScript事件代码:
>>1.HTML事件属性可以直接执行JavaScript代码
>>2.HTML事件属性可以调用JavaScript函数
>>3.可以为HTML元素指定自己的事件处理程序
>>3.可以组织事件的发生
>>等等...

## JavaScript 字符串
## 鼠标移入和移出事件
>特点:阻止冒泡
>onmouseenter:鼠标移入
>onmouseleave :鼠标移除
>特点:有冒泡()
>onmouseover:鼠标移入
>onmouseout:鼠标移除
>冒泡:(子元素触发某个类型的事件后,该元素的父级以及先辈触发同类事件)

## JavaScript typeof, null, 和 undefined
>### typeof 操作符
>你可以使用 typeof 操作符来检测变量的数据类型。
>ps:在JavaScript中，数组是一种特殊的对象类型。 因此 typeof [1,2,3,4] 返回 object。 
>### null
>在 JavaScript 中 null 表示 "什么都没有"。null是一个只有一个值的特殊类型。表示一个空对象引用。
>ps:用 typeof 检测 null 返回是object。
>### undefined
>在 JavaScript 中, undefined 是一个没有设置值的变量。
>typeof 一个没有值的变量会返回 undefined。
>ps:任何变量都可以通过设置值为 undefined 来清空。 类型为 undefined.
>undefined 和 null 的区别
实例
null 和 undefined 的值相等，但类型不等：
typeof undefined             // undefined
typeof null                  // object
null === undefined           // false
null == undefined            // true

## JavaScript 类型转换
>在 JavaScript 中有 5 种不同的数据类型：
>string,number,boolean,object,function
>3 种对象类型：Object,Date,Array
>2 个不包含任何值的数据类型：null,undefined
>### ps:
>NaN 的数据类型是 number
>数组(Array)的数据类型是 object
>日期(Date)的数据类型为 object
>null 的数据类型是 object
>未定义变量的数据类型为 undefined
>### constructor 属性
>constructor 属性返回所有 JavaScript 变量的构造函数。
>>#### 实例一:
>```javascript
>"John".constructor                 // 返回函数 String()  { [native code] }
>(3.14).constructor                 // 返回函数 Number()  { [native code] }
>false.constructor                  // 返回函数 Boolean() { [native code] }
>[1,2,3,4].constructor              // 返回函数 Array()   { [native code] }
>{name:'John', age:34}.constructor  // 返回函数 Object()  { [native code] }
>new Date().constructor             // 返回函数 Date()    { [native code] }
>function () {}.constructor         // 返回函数 Function(){ [native code] }
>```
>
>>#### 实例二
>可以使用 constructor 属性来查看对象是否为数组 (包含字符串 "Array"):
>
>```javascript
>function isArray(myArray) {
>return myArray.constructor.toString().indexOf("Array") > -1;
>}
>```
>>#### 实例三:
>可以使用 constructor 属性来查看对象是否为日期 (包含字符串 "Date"):
>```javascript
>function isDate(myDate) {
>return myDate.constructor.toString().indexOf("Date") > -1;
>}
>```
### JavaScript 类型转换
>JavaScript 变量可以转换为新变量或其他数据类型：
>通过使用 JavaScript 函数
>通过 JavaScript 自身自动转换
>#### 将数字转换为字符串
>全局方法 String() 可以将数字转换为字符串。
>该方法可用于任何类型的数字，字母，变量，表达式：
>实例:
>
>```javascript
>String(x)         // 将变量 x 转换为字符串并返回
>String(123)       // 将数字 123 转换为字符串并返回
>String(100 + 23)  // 将数字表达式转换为字符串并返回
>```
>Number 方法 toString() 也是有同样的效果。
>实例:
>
>```javascript
>x.toString()
>(123).toString()
>(100 + 23).toString()
>```
>数字转换为字符串的方法：
>|方法|描述|
>|:----|:----|
>|toExponential()|把对象的值转换为指数计数法。|
>|toFixed()|把数字转换为字符串，结果的小数点后有指定位数的数字。|
>|toPrecision()|把数字格式化为指定的长度。|
#### 将布尔值转换为字符串
>全局方法 String() 可以将布尔值转换为字符串。
>实例:
>```javascript
>String(false)        // 返回 "false"
>String(true)         // 返回 "true"
>```
>Boolean 方法 toString() 也有相同的效果。
>实例:
>
>```
>false.toString()     // 返回 "false"
>true.toString()      // 返回 "true"
>```
#### 将日期转换为字符串
>Date() 返回字符串。
>实例:
>```javascript
>Date()      // 返回 Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)
>```
>全局方法 String() 可以将日期对象转换为字符串。
>
>```javascript
>String(new Date())      // 返回 Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)
>```
>Date 方法 toString() 也有相同的效果。
>实例
>
>```
>obj = new Date()
>obj.toString()   // 返回 Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)
>```
>日期转换为字符串的函数：
>|方法|描述|
>|:---|:---|
>|getDate()|从 Date 对象返回一个月中的某一天 (1 ~ 31)。|
>|getDay()|从 Date 对象返回一周中的某一天 (0 ~ 6)。|
>|getFullYear()|从 Date 对象以四位数字返回年份。|
>|getHours()|返回 Date 对象的小时 (0 ~ 23)。|
>|getMilliseconds()|返回 Date 对象的毫秒(0 ~ 999)。|
>|getMinutes()|返回 Date 对象的分钟 (0 ~ 59)。|
>|getMonth()|从 Date 对象返回月份 (0 ~ 11)。|
>|getSeconds()|返回 Date 对象的秒数 (0 ~ 59)。|
>|getTime()|返回 1970 年 1 月 1 日至今的毫秒数。|
#### 将字符串转换为数字
>全局方法 Number() 可以将字符串转换为数字。
>字符串包含数字(如 "3.14") 转换为数字 (如 3.14).
>空字符串转换为 0。
>其他的字符串会转换为 NaN (不是个数字)。
>实例:
>
>```javascript
>Number("3.14")    // 返回 3.14
>Number(" ")       // 返回 0
>Number("")        // 返回 0
>Number("99 88")   // 返回 NaN
>```
>字符串转为数字的方法：
>|方法|描述|
>|:----|:----|
>|parseFloat()|解析一个字符串，并返回一个浮点数。|
>|parseInt()|解析一个字符串，并返回一个整数。|
#### 一元运算符 +
>Operator + 可用于将变量转换为数字：
>实例:
>
>```javascript
>var y = "5";      // y 是一个字符串
>var x = + y;      // x 是一个数字
>```
>如果变量不能转换，它仍然会是一个数字，但值为 NaN (不是一个数字):
>
>```javascript
>实例
>var y = "John";   // y 是一个字符串
>var x = + y;      // x 是一个数字 (NaN)
>```
#### 将布尔值转换为数字
>全局方法 Number() 可将布尔值转换为数字。
>实例:
>
>```javascript
>Number(false)     // 返回 0
>Number(true)      // 返回 1
>```
#### 将日期转换为数字
>全局方法 Number() 可将日期转换为数字。
>实例:
>
>```javascript
>d = new Date();
>Number(d)          // 返回 1404568027739
>```
>日期方法 getTime() 也有相同的效果。
>实例:
>```javascript
>d = new Date();
>d.getTime()        // 返回 1404568027739
>```
#### 自动转换类型
>当 JavaScript 尝试操作一个 "错误" 的数据类型时，会自动转换为 "正确" 的数据类型。
以下输出结果不是你所期望的：
实例:
5 + null    // 返回 5         null 转换为 0
"5" + null  // 返回"5null"   null 转换为 "null"
"5" + 1     // 返回 "51"      1 转换为 "1" 
"5" - 1     // 返回 4         "5" 转换为 5
##### 自动转换为字符串
>当你尝试输出一个对象或一个变量时 JavaScript 会自动调用变量的 toString() 方法：
>实例:
>
>```javascript
>document.getElementById("demo").innerHTML = myVar;
>myVar = {name:"Fjohn"}  // toString 转换为 "[object Object]"
>myVar = [1,2,3,4]       // toString 转换为 "1,2,3,4"
>myVar = new Date()      // toString 转换为 "Fri Jul 18 2014 09:08:55 GMT+0200"
>```
>数字和布尔值也经常相互转换：
>实例:
>
>```javascript
>myVar = 123             // toString 转换为 "123"
>myVar = true            // toString 转换为 "true"
>myVar = false           // toString 转换为 "false"
>```

## JavaScript正则表达式
>正则表达式（英语：Regular Expression，在代码中常简写为regex、regexp或RE）使用单个字符串来描述、匹配一系列符合某个句法规则的字符串搜索模式。
搜索模式可用于文本搜索和文本替换。

###  什么是正则表达式？
>正则表达式是由一个字符序列形成的搜索模式。
当你在文本中搜索数据时，你可以用搜索模式来描述你要查询的内容。
正则表达式可以是一个简单的字符，或一个更复杂的模式。
正则表达式可用于所有文本搜索和文本替换的操作。

###　语法
>/正则表达式主体/修饰符(可选)
其中修饰符是可选的。
实例：
var patt = /runoob/i
实例 解析：
/runoob/i  是一个正则表达式。
runoob  是一个正则表达式主体 (用于检索)。
i  是一个修饰符 (搜索不区分大小写)。 

### 使用字符串方法
>在 JavaScript 中，正则表达式通常用于两个字符串方法 : search() 和 replace()。
search() 方法 用于检索字符串中指定的子字符串，或检索与正则表达式相匹配的子字符串，并返回子串的起始位置。
replace() 方法 用于在字符串中用一些字符替换另一些字符，或替换一个与正则表达式匹配的子串。

### search() 方法使用正则表达式
>实例
>使用正则表达式搜索 "Runoob" 字符串，且不区分大小写：
>
>```javascript
>var str = "Visit Runoob!"; 
>var n = str.search(/Runoob/i);
>```

### search() 方法使用字符串
>search 方法可使用字符串作为参数。字符串参数会转换为正则表达式：
>实例
>检索字符串中 "Runoob" 的子串：
>
>```
>var str = "Visit Runoob!"; 
>var n = str.search("Runoob");
>```

### replace() 方法使用正则表达式
>实例:
>使用正则表达式且不区分大小写将字符串中的Microsoft替换为Runoob
>
>```javascript
>var str = document.getElementByid("demo").innerHTML;
>var txt = str.replace(/microsoft/i,"Runoob");
>```

### replace() 方法使用字符串
>replace() 方法将接收字符串作为参数：
>
>```javascript
>var str = document.getElementById("demo").innerHTML; 
>var txt = str.replace("Microsoft","Runoob");
>```
>ps:
>正则表达式参数可用在以上方法中 (替代字符串参数)。
正则表达式使得搜索功能更加强大(如实例中不区分大小写)。

### 正则表达式修饰符
>修饰符可在全局搜索中不区分大小写:
>
>| 修饰符 | 描述                                                 |
>| ------ | ---------------------------------------------------- |
>| i      | 执行对大小写不敏感的匹配                             |
>| g      | 执行全局匹配(查找所有匹配而非在找到第一个匹配后停止) |
>| m      | 执行多行匹配                                         |
>

### 正则表达式模式
>方括号用于查找某个范围内的字符：
>
>| 表达式 | 描述                     |
>| ------ | ------------------------ |
>| [abc]  | 查找方括号之间的任何字符 |
>| [0-9]  | 查找任何从0至9的数字     |
>| (x\|y) | 查找任何以\|分隔的选项   |
>
>元字符是拥有特殊含义的字符:
>
>| 元字符 | 描述                                    |
>| ------ | --------------------------------------- |
>| \d     | 查找数字                                |
>| \s     | 查找空白字符                            |
>| \d     | 匹配单词边界                            |
>| \uxxxx | 查找以十六进制数的xxxx规定的Unicode字符 |
>
>量词:
>
>| 量词 | 描述                            |
>| ---- | ------------------------------- |
>| n+   | 匹配任何包含至少一个n的字符     |
>| n*   | 匹配任何包含零个或多个n的字符   |
>| n?   | 匹配任何包含零个或一个n的字符串 |
>

### 使用 RegExp 对象
>在 JavaScript 中，RegExp 对象是一个预定义了属性和方法的正则表达式对象。

### 使用 test()
>test() 方法是一个正则表达式方法。
>test() 方法用于检测一个字符串是否匹配某个模式，如果字符串中含有匹配的文本，则返回 true，否则返回 false。
>以下实例用于搜索字符串中的字符 "e"：
>实例一:
>
>```javascript
>var patt = /e/;
>patt.test("The best things in life are free!");`
>```
>字符串中含有 "e"，所以该实例输出为：
>true
>
>案例二:
/e/.test("The best things in life are free!")

### 使用 exec()
>exec() 方法是一个正则表达式方法。
>exec() 方法用于检索字符串中的正则表达式的匹配。
>该函数返回一个数组，其中存放匹配的结果。如果未找到匹配，则返回值为 null。
>以下实例用于搜索字符串中的字母 "e":
>实例:
>
>```javascript
>/e/.exec("The best things in life are free!");
>```
>字符串中含有 "e"，所以该实例输出为:
e
>

## JavaScript JSON
>JSON 是用于存储和传输数据的格式。
JSON 通常用于服务端向网页传递数据 。

### 什么是 JSON?
>JSON 英文全称 JavaScript Object Notation
JSON 是一种轻量级的数据交换格式。
JSON是独立的语言 *
JSON 易于理解。

### JSON 实例
>以下 JSON 语法定义了 sites 对象: 3 条网站信息（对象）的数组:
>JSON 实例:
>
>```javascript
>{"sites":[
>    {"name":"Runoob", "url":"www.runoob.com"}, 
>    {"name":"Google", "url":"www.google.com"},
>    {"name":"Taobao", "url":"www.taobao.com"}
>]}
>```

###　JSON 格式化后为 JavaScript 对象
>JSON 格式在语法上与创建 JavaScript 对象代码是相同的。
由于它们很相似，所以 JavaScript 程序可以很容易的将 JSON 数据转换为 JavaScript 对象。

### JSON 语法规则
>数据为 键/值 对。
数据由逗号分隔。
大括号保存对象
方括号保存数组

### JSON 数据 - 一个名称对应一个值
>JSON 数据格式为 键/值 对，就像 JavaScript 对象属性。
>键/值对包括字段名称（在双引号中），后面一个冒号，然后是值：
>
>```javascript
>"name":"Runoob"
>```

### JSON 对象
>JSON 对象保存在大括号内。
>就像在 JavaScript 中, 对象可以保存多个 键/值 对：
>
>```
>{"name":"Runoob", "url":"www.runoob.com"}
>```

### JSON 数组
>JSON 数组保存在中括号内。
>就像在 JavaScript 中, 数组可以包含对象：
>
>```javascript
>"sites":[
>    {"name":"Runoob", "url":"www.runoob.com"}, 
>    {"name":"Google", "url":"www.google.com"},
>    {"name":"Taobao", "url":"www.taobao.com"}
>]
>```
>
>在以上实例中，对象 "sites" 是一个数组，包含了三个对象。
>每个对象为站点的信息（网站名和网站地址）。

### JSON 字符串转换为 JavaScript 对象
>通常我们从服务器中读取 JSON 数据，并在网页中显示数据。
>简单起见，我们网页中直接设置 JSON 字符串 (你还可以阅读我们的 JSON 教程):
>首先，创建 JavaScript 字符串，字符串为 JSON 格式的数据：
>
>```javascript
>var text = '{ "sites" : [' +
>'{ "name":"Runoob" , "url":"www.runoob.com" },' +
>'{ "name":"Google" , "url":"www.google.com" },' +
>'{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
>```
>
>然后，使用 JavaScript 内置函数 JSON.parse() 将字符串转换为 JavaScript 对象:
>
>```javascript
>var obj = JSON.parse(text);
>```
>
>最后，在你的页面中使用新的 JavaScript 对象：
>实例：
>
>```javascript
>var text = '{ "sites" : [' +
>    '{ "name":"Runoob" , "url":"www.runoob.com" },' +
>    '{ "name":"Google" , "url":"www.google.com" },' +
>    '{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
>    
>obj = JSON.parse(text);
>document.getElementById("demo").innerHTML = obj.sites[1].name + " " + obj.sites[1].url;
>```

### 相关函数
>| 函数             | **描述**                                       |
>| ---------------- | ---------------------------------------------- |
>| JSON.parse()     | 用于将一个 JSON 字符串转换为 JavaScript 对象。 |
>| JSON.stringify() | 用于将 JavaScript 值转换为 JSON 字符串。       |

## AJAX
### Ajax简介
>全称: Asynchronous JavaScript And XML
>异步的JavaScript和XML(可扩展标记语言)

### HTTP原理简介
>HTTP意为"超文本传输协议",web开发中最重要的网络协议
>访问网页的原理:请求 和 响应
>请求: 从客户端到服务器端的请求消息;响应:服务器根据客户的请求返回的内容

#### 请求方式:
>请求方式常见的有GET和POST方式
>GET方式请求:需要从服务器获取数据
>POST方式请求:把客户端的数据提交给服务器

#### 总结:
>Ajax就是通过运行JavaScript程序来发起HTTP请求,而不用非得把请求地址写到浏览器地址例再按回车

### 搭建自己的Web服务器(windows下)
>如何让自己的电脑变成服务器:安装Web服务器程序
>最常用的Web服务器程序:Apache
>安装集成环境:XAMPP(下载地址:www.xampps.com)

### Ajax使用步骤
>1. 创建XMLHttpRequest对象
>
>2. 使用事件监听请求过程的变化并设置回调函数处理响应内容
>
>3. 初始化请求
>
>4. 发送请求
>  HTML DOM querySelector() 方法:
>  定义和用法
>  querySelector() 方法返回文档中匹配指定 CSS 选择器的一个元素。
>  注意： querySelector() 方法仅仅返回匹配指定选择器的第一个元素。如果你需要返回所有的元素，请使用 querySelectorAll() 方法替代。
>  Ajax实例:
>
>  ```javascript
>  <script>
>  	//发起ajax请求
>  	//创建XMLHttpRequest对象
>  	var xhr = new XMLHttpRequest();
>  	// 设置 readystatechange事件 监听请求的过程
>  	/*
>  		* readyState 属性
>  		* 0 初始化值
>  		* 1 请求初始化完成后
>  		* 2 正式发出请求后
>  		* 3 开始接收到服务器的响应,但是还没有接收完全
>  		* 4 完全接收了响应
>  	*/
>  	xhr.onreadystatechange = function(){
>  		//判断成功接收了服务器的响应
>          //console.log(xhr.status};  //服务器状态码  200(成功)
>          if(xhr.status === 200 && xhr.readyState === 4){
>              console.log(xhr.responseText);
>          }
>  	}
>  	
>  	//请求初始化
>  	/**
>  		* 参数一 请求方式 GET 或 POST
>  		*参数二 请求的URL
>  		*参数三 是否异步 true/false 默认:true
>  	*/
>  	xhr.open("GET","URL",true);
>  	//发起请求
>  	/*
>  	 * get方式 send无需指定方式
>  	*/
>  	xhr.send();
>  <script>
>  ```

### XMLHttpRequest对象的属性
>|方法|描述|
>|:-----|:------|
>|open(method,url,async,uname,pswd)|规定请求的类型,URL,请求是否应该进行异步处理,以及请求的其他可选属性.<br />method:请求的类型:GET或POST<br />url:文件在服务器上的位置<br />async:true(异步)或false(同步)|
>|send(string)|发送请求到服务器.<br />string:仅用于POST请求|
>|setRequestHeader()|是设置HTTP请求头部的方法。此方法必须在 open() 方法和 send()之间调用。如果多次对同一个请求头赋值，只会生成一个合并了多个值的请求头。|
>|onreadystatechange|存储函数(或函数的名称)在每次readyState属性变化时被自动调用.(事件)|
>|readyState|存放了XMLHttpRequest的状态.从0到4变化:<br />0:请求未初始化<br />1:服务器建立链接<br />2:收到的请求<br />3:处理请求<br />4:请求完成和响应准备就绪|
>|status|返回状态数(例如"404"为"Not Found"或"200"为"OK")|
>|responseText|返回作为一个字符串的响应数据|
>

### Ajax发送post请求