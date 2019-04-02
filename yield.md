

```python
#Fibonacci斐波那契数列  生成
def fab(max):
    n, a, b = 0, 0, 1
    while n <  max:
        print(b)
        a, b = b, a+b
        n += 1
       
fab(5)
```

    1
    1
    2
    3
    5
    


```python
#改进，用List代替数列，提高fab函数可复用性
def fab(max):
    n, a, b = 0, 0, 1
    L=[]
    while n <  max:
        L.append(b)
        a, b = b, a+b
        n += 1
    return L
       
for i in fab(5):
    print(i)
    
#fab(5)
```

    1
    1
    2
    3
    5
    


```python
#List虽然提高了可复用性，但如果要控制内存占用，最好不要用List
#使用iterable来迭代，但麻烦不简洁
#引入yield函数
def fab(max):
    n, a, b = 0, 0, 1
    while n <  max:
        yield(b)
        a, b = b, a+b
        n += 1
       
#调用fab(5)，返回的是一个iterable对象
for i in fab(5):
    print(i)
```

    1
    1
    2
    3
    5
    

# yield函数
#### 简单的讲，yield的作用就是将一个函数变成一个genertor(生成器),带有 yield 的函数不再是一个普通函数，Python 解释器会将其视为一个 generator，调用 fab(5) 不会执行 fab 函数，而是返回一个 iterable 对象！在 for 循环执行时，每次循环都会执行 fab 函数内部的代码，执行到 yield b 时，fab 函数就返回一个迭代值，下次迭代时，代码从 yield b 的下一条语句继续执行，而函数的本地变量看起来和上次中断执行前是完全一样的，于是函数继续执行，直到再次遇到 yield。
#### 当函数执行结束时，generator 自动抛出 StopIteration 异常，表示迭代完成。在 for 循环里，无需处理 StopIteration 异常，循环会正常结束。
#### yield 的好处:把一个函数改写为一个 generator 就获得了迭代能力，比起用类的实例保存状态来计算下一个 next() 的值，不仅代码简洁，而且执行流程异常清晰。
