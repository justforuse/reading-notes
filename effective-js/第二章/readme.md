## 第2章 变量作用域

### 8 尽量少用全局对象

![image](https://user-images.githubusercontent.com/11868477/118390408-838beb00-b661-11eb-8d33-f037c1ec5cbf.png)

### 9 尽量声明局部变量

![image](https://user-images.githubusercontent.com/11868477/118391195-a8825d00-b665-11eb-8d3b-1f283d7cde98.png)

养成良好的编码习惯就好，声明变量始终使用var, let, const

### 10 避免使用with

![image](https://user-images.githubusercontent.com/11868477/118391778-acfc4500-b668-11eb-8d9a-33ccd6f64a91.png)

个人认为使用with的初衷就是快速访问with对象上的属性，当前就可以使用对象解构来代替了。

```js
let a = 'outer';
let obj = {
  a: 'inner'
}

function func() {
  with(obj) {
    console.log('a: ', a)
  }
}

func() // 'inner'  优先with对象上寻找变量
```

### 11 熟练掌握闭包

![image](https://user-images.githubusercontent.com/11868477/118392395-28abc100-b66c-11eb-8e42-e3435325b9c8.png)

![image](https://user-images.githubusercontent.com/11868477/118392404-2f3a3880-b66c-11eb-9108-d49b53cc395d.png)

实际场景经常用到，比如生成工具方法


### 12 理解变量声明提升

![image](https://user-images.githubusercontent.com/11868477/118393206-7296a600-b670-11eb-8b1a-4d68defedb84.png)

主要是var的特性，改用let, const可以规避大部分问题。

### 13 使用立即调用的函数表达式创建局部作用域

![image](https://user-images.githubusercontent.com/11868477/118393447-c8b81900-b671-11eb-9ae4-05bceed8d787.png)

同上，使用let, const也能解决缺少会计作用域的问题

### 14 当心命名函数表达式笨拙的作用域

![image](https://user-images.githubusercontent.com/11868477/118397462-b3011e80-b686-11eb-8f60-3023a6148aa1.png)

![image](https://user-images.githubusercontent.com/11868477/118485491-194f7500-b74b-11eb-91e9-e753116dbb7b.png)

描述了一些旧环境奇怪的表现，值得关注的是作者推荐避免命名函数

```js
// bad
const func = function bar(){
  // xxx
}

// good
const func = function() {
  // xxx
}

```

### 15 当心局部块函数声明笨拙的作用域

![image](https://user-images.githubusercontent.com/11868477/118486640-6b44ca80-b74c-11eb-97da-5232ec8d33e6.png)

避免在局部块或子语句中声明函数

### 16 避免使用eval创建局部变量

![image](https://user-images.githubusercontent.com/11868477/118487350-34bb7f80-b74d-11eb-9d87-8d589d2d7bba.png)

eval甚至都不推荐使用了, 目前个人也没有遇到使用场景

### 17 间接调用eval函数优于直接调用

![image](https://user-images.githubusercontent.com/11868477/118487732-9845ad00-b74d-11eb-9d50-57913fd1ad89.png)








