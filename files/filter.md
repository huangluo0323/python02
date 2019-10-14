# 1.3 filter方法

Python内建的**filter()函数用于过滤序列**。

> filter(function or None, iterable) --> filter object
>
> 和map()类似，filter()也接收一个函数和一个可迭代对象。和map()不同的是，filter()把传入的函数依次作用于每个元素，然后根据返回值是True还是False决定保留还是丢弃该元素。True保留，False丢弃 。

```python
a=filter(lambda x:x%2,[1,2,3,4,5,6,7,8]) #奇数
list(a)

res = filter(lambda s:s and s.strip(),['A','',None,'B','  ','C'])#去除空字符串
```



