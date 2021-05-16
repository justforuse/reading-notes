# Effective js

## 第1章 让自己习惯JavaScript

### 6 了解分号插入的局限

![image](https://user-images.githubusercontent.com/11868477/118389323-14f85e80-b65c-11eb-9146-94f4119bdf41.png)

看个人或者项目习惯吧，如果不让加分号有时候比较蛋疼


### 7 视字符串为16位的代码单元序列

![image](https://user-images.githubusercontent.com/11868477/118390018-7ec63780-b65f-11eb-93af-2c466359b1c2.png)

谨慎处理包含特殊且不常见的字符


## 第2章 变量作用域

### 尽量少用全局对象

![image](https://user-images.githubusercontent.com/11868477/118390408-838beb00-b661-11eb-8d33-f037c1ec5cbf.png)

### 尽量声明局部变量

![image](https://user-images.githubusercontent.com/11868477/118391195-a8825d00-b665-11eb-8d3b-1f283d7cde98.png)

养成良好的编码习惯就好，声明变量始终使用var, let, const

### 避免使用with

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
