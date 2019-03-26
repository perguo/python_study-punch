实现两个列表相加
===

'''

l1=[1,2,3,4,5]
l2=[11,22,33,44,55]
l3=l1+l2
#显示为列表合并
print(l3)
#如何实现列表值相加？
l=[]
for i,j in zip(l1,l2):
    sum=i+j
    l.append(sum)
print(l)
'''
