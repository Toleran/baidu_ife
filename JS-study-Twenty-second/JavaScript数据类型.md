### JavaScript 数据类型
字符串、数字、布尔、数组、对象、Null、Undefined

**JavaScript 拥有动态类型**

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：
实例

	var x                // x 为 undefined
	var x = 6;           // x 为数字
	var x = "Bill";      // x 为字符串


### JavaScript 字符串

字符串是存储字符（比如 "Bill Gates"）的变量。

字符串可以是引号中的任意文本。您可以使用单引号或双引号：
实例

	var carname="Bill Gates";
	var carname='Bill Gates';

您可以在字符串中使用引号，只要不匹配包围字符串的引号即可：


### JavaScript 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：
实例

	var x1=34.00;      //使用小数点来写
	var x2=34;         //不使用小数点来写

极大或极小的数字可以通过科学（指数）计数法来书写：
实例

	var y=123e5;      // 12300000
	var z=123e-5;     // 0.00123

### JavaScript 布尔

布尔（逻辑）只能有两个值：true 或 false。

	var x=true
	var y=false

布尔常用在条件测试中。

## JavaScript 数组

下面的代码创建名为 cars 的数组：

	var cars=new Array();
	cars[0]="Audi";
	cars[1]="BMW";
	cars[2]="Volvo";

或者 (condensed array):

	var cars=new Array("Audi","BMW","Volvo");

或者 (literal array):

	var cars=["Audi","BMW","Volvo"];
数组下标是基于零的，所以第一个项目是 [0]，第二个是 [1]，


### JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式
 (name : value) 来定义。属性由逗号分隔：

	var person={firstname:"Bill", lastname:"Gates", id:5566};

上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

空格和折行无关紧要。声明可横跨多行：

	var person={
	firstname : "Bill",
	lastname  : "Gates",
	id        :  5566
	};

**对象属性有两种寻址方式：**


	name=person.lastname;
	name=person["lastname"];


## Undefined 和 Null

Undefined 这个值表示变量不含有值。

可以通过将变量的值设置为 null 来清空变量。
实例

	cars=null;
	person=null;


### 声明变量类型

当您声明新变量时，可以使用关键词 "new" 来声明其类型：

	var carname=new String;
	var x=      new Number;
	var y=      new Boolean;
	var cars=   new Array;
	var person= new Object;

JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。