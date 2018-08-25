# 对象

#### 对象的定义
&emsp;&emsp;对象是JavaScript的一个基本数据类型，是一种复合值，它将很多值（原始值或者其他对象）聚合在一起，可通过名字访问这些值。即属性的无序集合  

#### 对象的创建（多种方法）
1、对象直接量 / 字面量  2、构造函数 　3、Object.create(原型)
##### 1、对象直接量 / 字面量
  ```js
 var obj = {
   name: 'lyl',
   age: 18
}
console.log(obj.name); // lyl
  ```
  
##### 2、构造函数
（1）、系统自带的的， eg： new Object(), Array(), Number(),Boolean(), Date()...
  ```js
 var obj = new Object();
      obj.name = 'lyl';
      console.log(obj.name); //lyl
  ```
（2）、自定义的：为了和普通函数区分，首字母大写，采用大驼峰式写法（普通函数采用小驼峰式写法）
  ```js
       function Obj (name) {
          this.name = name;
          this.age = 18;
      }
      var obj = new Obj('lyl');
      console.log(obj.name); //lyl
      console.log(obj.age); //18
  ``` 
##### 3、Object.create(原型)； 创建一个继承该原型的实例对象
  
  