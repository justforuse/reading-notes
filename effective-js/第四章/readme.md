## 第4章 对象和原型

### 30 理解prototype、getPrototypeOf和__proto__之间的不同

![image](https://user-images.githubusercontent.com/11868477/118661679-edeb8980-b821-11eb-8be4-1c84c70e45c9.png)

![image](https://user-images.githubusercontent.com/11868477/118792131-f0a1b980-b8c9-11eb-88ab-5b4d9a9b5a61.png)

![image](https://user-images.githubusercontent.com/11868477/118792152-f5ff0400-b8c9-11eb-96c6-df683f26d2ab.png)

![image](https://user-images.githubusercontent.com/11868477/118792180-fdbea880-b8c9-11eb-9ccd-175fc6e3b648.png)

### 31 使用Object.getPrototypeOf函数而不是使用__proto__属性

![image](https://user-images.githubusercontent.com/11868477/118792980-be448c00-b8ca-11eb-8620-b128f682082d.png)

前者符合标准

### 32 始终不要修改__proto__属性

![image](https://user-images.githubusercontent.com/11868477/118793218-f8ae2900-b8ca-11eb-8532-a910c7ddfde5.png)

### 33 使构造函数与new操作符无关

![image](https://user-images.githubusercontent.com/11868477/118793618-5cd0ed00-b8cb-11eb-87f6-92caa0f3890b.png)

Object.create()方法创建一个新对象，使用现有的对象来提供新创建的对象的__proto__。

关于Object.create的[MDN文档](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

### 34 在原型中存储方法

![image](https://user-images.githubusercontent.com/11868477/118795113-d6b5a600-b8cc-11eb-8396-0b8297fc0581.png)

### 35 使用闭包存储私有数据

![image](https://user-images.githubusercontent.com/11868477/118795934-b0dcd100-b8cd-11eb-988a-66419a251576.png)

### 36 只将实例状态存储在实例对象中

![image](https://user-images.githubusercontent.com/11868477/118796240-00230180-b8ce-11eb-9f1d-20aa00fc5c5d.png)

### 37 认识到this变量的隐式绑定问题

![image](https://user-images.githubusercontent.com/11868477/118798488-47aa8d00-b8d0-11eb-84ad-0efa54c7df81.png)


### 38 在子类的构造函数中调用父类的构造函数

![image](https://user-images.githubusercontent.com/11868477/118799465-5776a100-b8d1-11eb-9e20-ee4297426669.png)

### 39 不要重用父类的属性名

![image](https://user-images.githubusercontent.com/11868477/118799991-fef3d380-b8d1-11eb-8deb-9e894a3e8062.png)

### 40 避免继承标准类

![image](https://user-images.githubusercontent.com/11868477/118800380-6c076900-b8d2-11eb-8b2c-29b86ac83ca6.png)

### 41 将原型视为实现细节

![image](https://user-images.githubusercontent.com/11868477/118800637-ba1c6c80-b8d2-11eb-8374-4f4934bc6ba5.png)

### 42 避免使用轻率的猴子补丁

![image](https://user-images.githubusercontent.com/11868477/118807417-de7c4700-b8da-11eb-8957-a5ac25366c41.png)

猴子补丁就是在原型上补全缺失的方法

















