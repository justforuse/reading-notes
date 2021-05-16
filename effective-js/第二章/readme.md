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
