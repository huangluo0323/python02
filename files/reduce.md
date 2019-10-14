# 1.2 reduce方法

> reduce(function, sequence[, initial])
>
> reduce把一个函数作用在一个序列上，从第一个元素开始把结果继续和序列的下一个元素做累积计算]

在 Python3 中，reduce() 函数已经被从全局名字空间里移除了，它现在被放置在 fucntools 模块里，如果想要使用它，则需要通过引入 functools 模块来调用 reduce() 函数：

```python
from functools import reduce

reduce(lambda x,y:x+y,[1,2,3,4,5,6])

#把序列[1, 3, 5, 7, 9]变换成整数13579
reduce(lambda x,y:x*10 + y,[1,3,5,7,9])
```

reduce函数可以设置initial，会先被计算

```python
from functools import reduce
reduce(lambda x,y:x+y,['x','y','z'],a)

scientists =({'name':'Alan Turing', 'age':105, 'gender':'male'},
              {'name':'Dennis Ritchie', 'age':76, 'gender':'male'},
              {'name':'Ada Lovelace', 'age':202, 'gender':'female'},
              {'name':'Frances E. Allen', 'age':84, 'gender':'female'})
def reducer(accumulator , value):
	sum = accumulator + value['age']
	return sum
total_age = reduce(reducer, scientists, 0)#在第一次计算时，accumulator为0
print(total_age)
```

