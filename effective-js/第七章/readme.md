## 第7章 并发

### 61 不要阻塞I/O事件队列

![image](https://user-images.githubusercontent.com/11868477/119097084-ea851780-ba46-11eb-8b34-1bfa9fd9eb97.png)

![image](https://user-images.githubusercontent.com/11868477/119097212-0dafc700-ba47-11eb-911b-efa48af4f0d1.png)

### 62 在异步序列中使用嵌套或命名的回调函数

![image](https://user-images.githubusercontent.com/11868477/119097626-8c0c6900-ba47-11eb-9179-93c7f01e94f6.png)

目前通常使用Promise或者Async/Await方式，解决链式异步调用

### 63 当心丢弃错误

![image](https://user-images.githubusercontent.com/11868477/119098110-105eec00-ba48-11eb-8fb8-d4776eb15877.png)

### 64对异步循环使用递归

![image](https://user-images.githubusercontent.com/11868477/119098467-7481b000-ba48-11eb-984c-9e8b2065768d.png)

### 65 不要在计算时阻塞事件队列

![image](https://user-images.githubusercontent.com/11868477/119101248-5a959c80-ba4b-11eb-8afc-3fdc272b631a.png)

### 66 使用计数器来执行并行操作

![image](https://user-images.githubusercontent.com/11868477/119101498-a21c2880-ba4b-11eb-82b5-d07da9edf557.png)

比如想自己实现Promise.all方法时，就需要在内部记录一个计数器，用来判断是否都执行完毕。

### 67 绝不要同步地调用异步的回调函数

![image](https://user-images.githubusercontent.com/11868477/119102005-28386f00-ba4c-11eb-9ab8-206ffd7e0ca6.png)

### 68 使用promise模式清洁异步逻辑

![image](https://user-images.githubusercontent.com/11868477/119102428-95e49b00-ba4c-11eb-9e1b-d94c9712c447.png)

这时介绍的还是promise库的方法，与es6标准的Promise差异较大，但基本思想都是使用then做流程控制

