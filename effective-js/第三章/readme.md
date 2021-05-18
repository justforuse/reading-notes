## 第3章 使用函数

### 18 理解函数调用、方法调用及构造函数调用之间的不同

![image](https://user-images.githubusercontent.com/11868477/118490554-a34e0c80-b750-11eb-99f6-90122eca2542.png)

![image](https://user-images.githubusercontent.com/11868477/118490781-e0b29a00-b750-11eb-8534-41f61a69bbac.png)

三种使用函数的场景，理解this的指向问题，this在被调用时指定

### 19 熟练掌握高阶函数

![image](https://user-images.githubusercontent.com/11868477/118492369-86b2d400-b752-11eb-90a7-74dc9a2cba11.png)

### 20 使用call方法自定义接收者来调用方法

![image](https://user-images.githubusercontent.com/11868477/118493428-ad253f00-b753-11eb-9b7d-f265b7e48021.png)

### 21 使用apply方法通过不同数量的参数调用函数

![image](https://user-images.githubusercontent.com/11868477/118581131-aa623280-b7c3-11eb-86ec-adbc1c9c97e6.png)

很多时候可以用数组解构来解决

```js
// before
Math.max.apply(null, [1,2,3]);

// now
Math.max(...[1,2,3])

```

### 22 使用arguments创建可变参数的函数

![image](https://user-images.githubusercontent.com/11868477/118584200-0e3b2a00-b7c9-11eb-9ad3-5cd0915e7598.png)

arguments是全参数，即便已经声明参数来接受，arguments依旧返回全量的参数列表，包含length属性，可以使用Array.from来转为真正的数组。

### 23 永远不要修改arguments对象

![image](https://user-images.githubusercontent.com/11868477/118586132-c74f3380-b7cc-11eb-8955-3d44c8e0eb6e.png)

> 所有命名参数都是arguments对象中对应索引的别名。

触及知识盲区了，，在修改arguments对象时会影响到后续参数的值。

```js

function func (a, b) {
  console.log(a, b, arguments); // 1, 2, [1,2,3]
  [].shift.call(arguments);
  // a 实际是arguments[0], b是arguments[1]
  console.log(a, b, arguments) // 2, 3, [2,3]
}

func(1, 2, 3);
```

### 24 使用变量保存arguments的引用

![image](https://user-images.githubusercontent.com/11868477/118626213-4197ac00-b7fd-11eb-839a-e38e64b0e9a9.png)

### 25 使用bind方法提取具有确定接收者的方法

![image](https://user-images.githubusercontent.com/11868477/118636367-33e72400-b807-11eb-9d09-4d0c5f9af14a.png)

### 26 使用bind方法实现函数柯里化

![image](https://user-images.githubusercontent.com/11868477/118648195-c0e4aa00-b814-11eb-92d8-da7ad1718254.png)

### 27 使用闭包而不是字符串来封装代码

![image](https://user-images.githubusercontent.com/11868477/118655353-0e184a00-b81c-11eb-9941-caf06c153a71.png)


### 28 不要信赖函数对象的toString方法

![image](https://user-images.githubusercontent.com/11868477/118655733-68190f80-b81c-11eb-80a6-ac85bfe80176.png)

### 29 避免使用非标准的栈检查属性

![image](https://user-images.githubusercontent.com/11868477/118656245-ef668300-b81c-11eb-98fa-37be43185650.png)





