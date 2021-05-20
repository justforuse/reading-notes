## 第5章

### 43 使用Object的直接实例构造轻量级的字典

![image](https://user-images.githubusercontent.com/11868477/118808467-22bc1700-b8dc-11eb-8a31-d22af64815de.png)

### 使用null原型以防止原型污染

![image](https://user-images.githubusercontent.com/11868477/118812258-7e889f00-b8e0-11eb-8bf0-14b475ec213d.png)

### 45 使用hasOwnProperty方法以避免原型污染

![image](https://user-images.githubusercontent.com/11868477/118812761-08d10300-b8e1-11eb-8d67-65bc06fdbda0.png)

### 46 使用数组而不要使用字典来存储有序集合

![image](https://user-images.githubusercontent.com/11868477/118814229-7e899e80-b8e2-11eb-8132-bdc1844825e6.png)

这种场景下可以使用Map，Map会根据设置的顺序输出结果

```js
const ratings = {
    'aaa': 0.8,
    'bbb': 0.7,
    '21': 0.6,
    'ddd': 0.9
}
let total = 0;
for (const name in ratings) {
    console.log(name); // 21 aaa bbb ddd
    total += ratings[name]
}
console.log(total) // 2.99....6

let total2 = 0;
const map = new Map();
map.set('aaa', 0.8);
map.set('bbb', 0.7);
map.set('21', 0.6);
map.set('ddd', 0.9);
for(const [key, value] of map.entries()) {
    console.log(key); // aaa bbb 21 ddd
    total2 += value;
}
console.log(total2); // 3
```

### 47 绝不要再Object.prototype中增加可枚举的属性

![image](https://user-images.githubusercontent.com/11868477/118816434-c01b4900-b8e4-11eb-899f-dd14e70e9f64.png)

使用defineProperty方法定义属性的“配置”

### 48 避免在枚举期间修改对象

![image](https://user-images.githubusercontent.com/11868477/118910726-951e0d00-b957-11eb-9c60-1a264f2a6d53.png)

### 49 数组迭代要优先使用for循环而不是for...in循环

![image](https://user-images.githubusercontent.com/11868477/118911041-16759f80-b958-11eb-925f-4796b5789c0f.png)

```js
// not good
for (let i = 0; i < arr.length; i++) {
  // xxx
}

// good
const arrLength = arr.length;
for (let i = 0; i < arrLength; i++) {
  // xxx
}

```

但对于此情况通常使用forEach代替。

### 50 迭代方法优于循环

![image](https://user-images.githubusercontent.com/11868477/118911686-3063b200-b959-11eb-99cb-56fcec59e932.png)

### 51 在类数组对象上复用通用的数组方法

![image](https://user-images.githubusercontent.com/11868477/118912548-87b65200-b95a-11eb-9f47-f925d236ff65.png)


![image](https://user-images.githubusercontent.com/11868477/118912411-5d649480-b95a-11eb-9931-46fe4539bb63.png)

es6可以使用Array.from方法转为一个真正的数组

### 52 数组字面量优于数组构造函数

![image](https://user-images.githubusercontent.com/11868477/118912720-c815d000-b95a-11eb-9bbc-555e298d18cf.png)
