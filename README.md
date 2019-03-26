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
