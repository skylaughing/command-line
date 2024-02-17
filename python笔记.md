<center><h1>Python</center>

- <h4>列表生成式
[http://t.csdnimg.cn/20i4L](http://t.csdnimg.cn/20i4L)

```python
list = [list_element for i in x if condition]
总结：列表生成式生成一个列表list,格式为list = 中括号[要append进列表元素+生成代码]，生成代码将原本竖着的代码改为横着顺序写
```

**例1：**
```python
list = [i*i for i in range(1,10) if i%2 == 0]

相当于：
list = []
for i in range(1,10):
    if i%2 == 0:
        list.append(i*i)
```

**例2：**
将矩阵li1转化成一个数组(列表),且使该数组中仅仅包含偶数：
li1 = [ [1, 2, 3],[4, 5, 6],[7, 8, 9] ]
```python
list = [j for i in li1 for j in i if j % 2 == 0]
list = [li1[i][j] for i in range(len(li1)) for j in range(len(li1[i])) if li1[i][j] % 2 == 0]
```

**例3：**
```python
from random import *
y = [randint(1,1000) for i in range(10)] # 取得10个1~999之间的随机数，放进列表y
print(y)

#绘制折线图
from matplotlib import pyplot as plt 
plt.plot(y)
plt.show()
```
