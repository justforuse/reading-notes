## 第6章 库和API设计

### 53 保持一致的约定

![image](https://user-images.githubusercontent.com/11868477/118914443-d1ed0280-b95d-11eb-993b-5f7be6b750b7.png)


### 54 将undefined看做“没有值”

![image](https://user-images.githubusercontent.com/11868477/118923272-de795700-b96d-11eb-84f0-b2dc144175e8.png)

### 55 接收关键字参数的选项对象

![image](https://user-images.githubusercontent.com/11868477/118952083-3758e780-b98e-11eb-98d0-2de861bc3484.png)

注意||的局限性，0，''等值会被认为假，应该检查是否为undefiend，或者可以使用??来设置默认值。

### 56 避免不必要的状态

![image](https://user-images.githubusercontent.com/11868477/118953970-e5b15c80-b98f-11eb-94c2-b7806a321c23.png)


![image](https://user-images.githubusercontent.com/11868477/118953939-dd592180-b98f-11eb-9b2c-ea281ef69b61.png)

### 57 使用结构类型设计灵活的接口

![image](https://user-images.githubusercontent.com/11868477/118956667-63766780-b992-11eb-934c-26326230dc59.png)

### 58 区分数组对象和类数组对象

![image](https://user-images.githubusercontent.com/11868477/118958529-17c4bd80-b994-11eb-8077-9734d5caeeda.png)

![image](https://user-images.githubusercontent.com/11868477/119078523-f19d2d00-ba28-11eb-87ed-75a7d0eb80c5.png)

### 59 避免过度的强制转换

![image](https://user-images.githubusercontent.com/11868477/119095906-772ed600-ba45-11eb-9a59-dc06aecdb098.png)

一般来说，对于函数的参数，都不应该在内部做修改。

### 60 支持方法链

![image](https://user-images.githubusercontent.com/11868477/119096082-b8bf8100-ba45-11eb-927f-28dbe0282671.png)

![image](https://user-images.githubusercontent.com/11868477/119096173-d1c83200-ba45-11eb-89b0-227607fa7354.png)

