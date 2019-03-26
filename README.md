实现两个列表相加
===

```
l1=[1,2,3,4,5]
l2=[11,22,33,44,55]
l3=l1+l2
#显示为列表合并
print(l3)
#如何实现列表值相加？
#方法1
l=[]
for i,j in zip(l1,l2):
    sum=i+j
    l.append(sum)
print(l)

#方法2
d=[]
for i in range(0,len(l1)):
    sum=l1[i]+l2[i]
    d.append(sum)
print(d)
```

        [1, 2, 3, 4, 5, 11, 22, 33, 44, 55]
        [12, 24, 36, 48, 60]
        [12, 24, 36, 48, 60]
        
## numpy.array()方法
  ```
  import numpy
a=numpy.array([1,2,3,4,5])
b=numpy.array([11,22,33,44,55])
c=a+b
print(list(c))
```

        [12, 24, 36, 48, 60]

# List(列表)
* del:删除
```
a = [1,2,3,4,5,6]
del a[2]
print(a)

# del一个变量后不能在继续使用此变量
del  a
print(a)
```
        [1, 2, 4, 5, 6]
        ---------------------------------------------------------------------------
        NameError                                 Traceback (most recent call last)
        <ipython-input-14-94bf5611738e> in <module>()
      1 del  a
        ----> 2 print(a)

        NameError: name 'a' is not defined
        
 * 链表的遍历
 *  for
 *  while
```
 # for in list
a = [1,2,3,4,5]

# 挨个打印a里边的元素
for i in a:
    print(i)
```
        1
        2
        3
        4
        5
```
#双层列表循环
#a 为嵌套列表，或者叫双层列表
a = [["one", 1], ["two", 2], ["three", 3] ]

for k,v in a:
    print(k, "--", v)
```
        one -- 1
        two -- 2
        three -- 3


# 关于列表的常用函数
## len:求列表长度
```
a = [x for x in range(1,100)]
print(len(a))

# max:求列表中的最大值
# min： 同理
print(max(a))

b = ['man', 'film', 'python']
print(max(b))
```
        99
        99
        python
        
## list：将其他格式的数据转换成list
```
a = [1,2,3]
print(list(a))

s = "I love wangxiaojing"
print(list(s))

# 把range产生的内容转换成list
#range()函数可创建一个整数列表，一般用在for循环中
print(list(range(12, 19)))

```
        [1, 2, 3]
        ['I', ' ', 'l', 'o', 'v', 'e', ' ', 'w', 'a', 'n', 'g', 'x', 'i', 'a', 'o', 'j', 'i', 'n', 'g']
        [12, 13, 14, 15, 16, 17, 18]
