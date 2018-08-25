# JS 的数据类型分类和判断

#### ECMAScript 6种原始类型
    1、Boolean
    2、 String 
    3、 Number
    4、 Null
    5、 Undefined
    6、 Symbol （es6）
	
#### 数据类型分为：值类型和引用类型   
    1、值类型变量包括 Boolean、String、Number、Undefined、Null  
    2、引用类型包括了 Object 类的所有，如 Date、Array、Function   

#### 类型判断的方法
1、**typeof**  

typeof只有区分值类型的详细类型

  ```js  
var x = 1;
console.log(typeof x);//number
 
var a = undefined;
console.log(typeof a);//undefined
 
var b = null;
console.log(typeof b);//object，（null是空对象引用/或者说指针）。
 
var c = new Object();
console.log(typeof c);//object
 
var e = [1,2,3];
console.log(typeof e);//object 
 
var d = function(){
 // ... 语句块
}
console.log(typeof d);//function
  ```


2、**instanceof**  
用于实例和构造函数的对应。例如判断一个变量是否是数组，使用typeof无法判断，但可以使用[1, 2] instanceof Array来判断。因为，[1, 2]是数组，它的构造函数就是Array。同理：  
  ```js
function Foo(name) {
    this.name = name
   }
var foo = new Foo('bar')
console.log(foo instanceof Foo) // true
  ```

#### 变量计算
    1、字符串拼接
    2、 “==”运算
    3、 if语句
    4、 逻辑运算符（&&与 ||或 ！非）


