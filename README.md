# 632107060224 曹主能
# JavaScript总结
## 基本语法
- JavaScript是大小写敏感的编程语言，标识符也需要注意大小写。
- 注释使用 // 或者 /* */ 的方式，可以提高代码的可读性。
- 关键字是该语言的保留字，包括：break、case、catch、continue、debugger、default、delete、do、else、finally、for、function、if、in、instanceof、new、return、switch、this、throw、try、typeof、var、void、while、with。
- 变量是用于存储数据的容器，可以通过 var、let、const 来声明变量。
## 操作符
- 一元操作符只需要一个操作数，例如 ++、--。
- 布尔操作符是用于逻辑判断，例如 &&、||、!。
- 算术操作符用于数学运算，例如 +、-、*、/。
- 关系操作符用于比较运算，例如 ==、!=、>、<、>=、<=。
- 条件操作符用于三元表达式，例如 ? : 。
- 赋值操作符用于给变量赋值，例如 =、+=、-=、*=、/= 等。
## 函数
- 函数是一段可重用的代码块，通过函数可以封装任意多条语句，而且可以在任何地方、任何时候调用执行。
- 函数可以有参数和返回值，通过传递参数和返回值可以更好地控制程序的流程。
- 函数声明的语法如下：
```
function functionName(arg1, arg2, ...) {
  // 函数体
}
```
可以通过函数名调用函数，例如：
```javascript
function add(a, b) {
  return a + b;
}
var result = add(1, 2);
console.log(result); // 输出：3
```
## 对象Object
- 对象是一种复合数据类型，可以用来存储不同类型的数据。
- 对象的属性和方法可以通过 . 或者 [] 来访问。
- 对象可以通过 new 关键字来实例化一个新的对象。
- 对象字面量的语法如下：
```javascript
var obj = {
  key1: value1,
  key2: value2,
  ...
};
```
构造函数的语法如下：
```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}
var person1 = new Person("Alice", 18);
var person2 = new Person("Bob", 20);
```
可以使用点号或者方括号来访问对象的属性，例如：
```javascript
var obj = { name: "Alice", age: 18 };
console.log(obj.name); // 输出：Alice
console.log(obj["age"]); // 输出：18
```
## 数组和数组方法
在 JavaScript 中，数组是一组值的有序集合，可以使用数组字面量或者构造函数来创建数组。
数组字面量的语法如下：
```javascript
var arr = [value1, value2, ...];
```
构造函数的语法如下：
```javascript
var arr = new Array(value1, value2, ...);
```
可以使用索引来访问数组中的元素，例如：
```javascript
var arr = [1, 2, 3];
console.log(arr[0]); // 输出：1
console.log(arr[1]); // 输出：2
console.log(arr[2]); // 输出：3
```
JavaScript 中有许多数组方法，它们可以用于对数组进行操作。下面介绍一些常用的数组方法。
### 元素联合方法
- concat()：用于合并两个或多个数组。
```javascript
var arr1 = [1, 2, 3];
var arr2 = [4, 5, 6];
var arr3 = arr1.concat(arr2);
console.log(arr3); // 输出：[1, 2, 3, 4, 5, 6]
```
### 堆栈方法
- push()：向数组的末尾添加一个或多个元素，并返回新的长度。
- pop()：从数组的末尾删除一个元素，并返回该元素。
```javascript
var arr = [1, 2, 3];
arr.push(4);
console.log(arr); // 输出：[1, 2, 3, 4]
arr.pop();
console.log(arr); // 输出：[1, 2, 3]
```
### 队列方法
- shift()：从数组的开头删除一个元素，并返回该元素。
- unshift()：向数组的开头添加一个或多个元素，并返回新的长度。
```javascript
var arr = [1, 2, 3];
arr.shift();
console.log(arr); // 输出：[2, 3]
arr.unshift(4);
console.log(arr); // 输出：[4, 2, 3]
```
### 反链接方法
- reverse()：将数组中的元素反转。
```javascript
var arr = [1, 2, 3];
arr.reverse();
console.log(arr); // 输出：[3, 2, 1]
```
### 分片方法
- slice()：从数组中选取一个子集。
```javascript
var arr = [1, 2, 3, 4, 5];
var arr2 = arr.slice(1, 4);
console.log(arr2); // 输出：[2, 3, 4]
```
## 链式语法
- 链式语法是指在一个语句中串联多个方法调用。
- 链式语法可以提高代码的可读性和可维护性。
- 链式语法的调用顺序是从左到右。
JavaScript 中的多个方法可以链式调用，例如：
```javascript
let arr = [1, 2, 3, 4, 5];
let even = arr.filter(function(num) {
  return num % 2 == 0;
}).map(function(num) {
  return num * 2;
}).reduce(function(sum, num) {
  return sum + num;
}, 0);
console.log(even); // 输出：12
```
这段代码首先调用了 filter() 方法，过滤出数组中的偶数，然后调用 map() 方法，将偶数乘以 2，最后调用 reduce() 方法，将乘以 2 的偶数相加。


# TypeScript总结
## TypeScript是什么
TypeScript是一种由微软开发的开源编程语言，它是JavaScript的超集，可以编译成纯JavaScript代码。TypeScript提供了一些JavaScript没有的特性，例如：静态类型、类、接口、命名空间等，这些特性可以帮助开发者编写更加稳定、易于维护的代码。

## TypeScript基础
### 基本语法
TypeScript的语法与JavaScript类似，但是它支持强类型。在TypeScript中，需要声明变量的类型。例如：
```typescript
let myName: string = "Alice";
let myAge: number = 30;
```
在上面的例子中，声明了一个字符串类型的变量`myName`，以及一个数字类型的变量`myAge`。在变量名后面，使用冒号和类型名称来声明变量类型。这个语法可以帮助在开发过程中更早地发现类型错误，从而减少代码错误。
### 基本数据类型
TypeScript支持JavaScript的所有原始数据类型，包括：
- 数字类型 Number
- 布尔类型 Boolean
- 字符串类型 String
- 空值类型 Void
- 空类型 Null 和 Undefined
同时，TypeScript还支持一些特殊的数据类型，例如 Any 和 Never。

### 变量声明
在TypeScript中，变量必须先声明才能使用。TypeScript的变量声明与JavaScript类似，但是它需要使用关键字 let 或 const 来声明变量。例如：
```typescript
let myName: string = "Alice";
const myAge: number = 30;
// 声明同时赋值
let myNumber: number = 5, myBoolean: boolean = true;
// 变量声明可以使用解构赋值
let [first, second, third] = [1, 2, 3];
let {name, age} = {name: "Alice", age: 30};
```
### 运算符
TypeScript支持JavaScript的所有运算符，包括：
- 算术运算符：`+`、`-`、`*`、`/`、`%`
- 比较运算符：`==`、`!=`、`===`、`!==`、`<`、`>`、`<=`、`>=`
- 逻辑运算符：`&&`、`||`、`!`
- 位运算符：`&`、`|`、`^`、`~`、`<<`、`>>`、`>>>`
```typescript
let myNumber: number = 5;
let isEqual: boolean = myNumber == 5;
let isGreater: boolean = myNumber > 3;
let result: number = 5 & 3;
```

## TypeScript条件语句
TypeScript条件语句与JavaScript条件语句类似，包括if、else if、else等关键字。例如：
```
let score: number = 80;
if(score >= 90) {
  console.log("优秀");
} else if(score >= 60) {
  console.log("及格");
} else {
  console.log("不及格");
}
```
## TypeScript循环语句
TypeScript循环与JavaScript循环类似，包括for、while、do while等关键字。例如：
```
for(let i = 0; i < 10; i++) {
  console.log(i);
}
let i: number = 0;
while(i < 10) {
  console.log(i);
  i++;
}
let j: number = 0;
do {
  console.log(j);
  j++;
} while(j < 10);
```
## TypeScript函数
TypeScript函数与JavaScript函数类似，但是需要声明函数的参数类型和返回值类型。例如：
```
function add(a: number, b: number): number {
  return a + b;
}
let result: number = add(5, 10);
```

## TypeScript类
TypeScript是一种面向对象的编程语言，它支持类的定义和使用，以及类的属性和函数的访问权限、存取器、静态属性、继承等特性。
### 定义和使用
在TypeScript中，可以使用 class 关键字定义一个类。例如：
```typescript
class Person {
  name: string;
  age: number;
  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
  sayHello(): void {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}
let alice: Person = new Person("Alice", 30);
alice.sayHello();
```
在上面的例子中，定义了一个 Person 类。它有两个属性，name 和 age，以及一个构造函数和一个 sayHello 方法。要创建类的实例，使用 new 关键字进行实例化，例如 `let alice: Person = new Person("Alice", 30);`。之后就可以调用实例的方法，例如 `alice.sayHello();`。
### 属性和函数的访问权限
在TypeScript中，可以使用 public、protected 和 private 关键字来控制类的属性和方法的访问权限。默认情况下，所有的属性和方法都是 public 的。
- public：公共的，可以在类的内部和外部被访问；
- protected：受保护的，只能在类的内部和子类中被访问；
- private：私有的，只能在类的内部被访问。
例如：
```typescript
class Person {
  public name: string;
  protected age: number;
  private gender: string;
  constructor(name: string, age: number, gender: string) {
    this.name = name;
    this.age = age;
    this.gender = gender;
  }
  sayHello(): void {
    console.log(`Hello, my name is ${this.name}.`);
    console.log(`I am ${this.age} years old.`);
    console.log(`I am a ${this.gender}.`);
  }
}
let alice: Person = new Person("Alice", 30, "female");
alice.sayHello(); // 输出：Hello, my name is Alice. I am 30 years old. I am a female.
```
在上面的例子中，定义了一个 Person 类和一个 Employee 类。Person 类有三个属性 name、age 和 gender，其中 name 是 public 的、age 是 protected 的、gender 是 private 的。还定义了一个 sayHello 方法来输出属性的内容。

### 静态属性
在TypeScript中，可以使用 static 关键字定义一个静态属性或方法。静态属性和方法不是针对实例的，而是针对类的。静态属性和方法可以通过类名进行访问，而不需要先实例化一个对象。例如：
```typescript
class Person {
  static species: string = "Homo sapiens";
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  sayHello(): void {
    console.log(`Hello, my name is ${this.name}.`);
  }
  static saySpecies(): void {
    console.log(`We are ${Person.species}.`);
  }
}
let alice: Person = new Person("Alice");
alice.sayHello(); // 输出：Hello, my name is Alice.
Person.saySpecies(); // 输出：We are Homo sapiens.
```
在上面的例子中，定义了一个 Person 类，并在其中定义了一个静态属性 species 和一个静态方法 saySpecies。可以通过 Person.species 来访问静态属性的值，通过 Person.saySpecies() 来调用静态方法。
### 继承
在TypeScript中，可以使用 extends 关键字来实现类的继承。子类会继承父类的属性和方法，并可以重写父类的方法。例如：
```typescript
class Animal {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
  move(distance: number = 0) {
    console.log(`${this.name} moved ${distance}m.`);
  }
}
class Dog extends Animal {
  bark() {
    console.log("Woof! Woof!");
  }
  move(distance: number = 5) {
    console.log(`${this.name} runs ${distance}m.`);
  }
}
let myDog: Dog = new Dog("Bobby");
myDog.bark(); // 输出：Woof! Woof!
myDog.move(); // 输出：Bobby runs 5m.
```
在上面的例子中，定义了一个 Animal 类和一个 Dog 类。Dog 类继承了 Animal 类，并实现了 bark 方法和重写了 move 方法。可以创建一个 Dog 的实例 myDog，并调用它的 bark 方法和 move 方法。在 myDog.move() 方法中，它会调用子类的 move 方法，而不是父类的 move 方法。
