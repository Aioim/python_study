### if/elif/else选择动作语句

```python
# 代码示例
str_text = 'python & C++'
if 'python' in str_text:
    print('python')
elif 'CSS' in str_text:
    print('CSS')
else:
    print('这是啥啊')
a = 0
for i in range(-10, 10):  # 三元表达式写法
    a += 1 if i > 0 else 2
    print(a, end=' ')
```



## while/else & for

```python
# 代码示例
t = 0
while t < 5:
    str_text = 'python & C++'
    for i in str_text:
        if i == 'p':
            print('P')
        if i == '&':
            continue
        if i == '=':
            break
        t += 1
else:
    print('非break执行退出')
```



## yield生成器函数

```python
def gen(n: int):  # 定义n为int类型，这样有利于提高代码的可读性 
    for i in range(n): yield i ** 2

for x in gen(10):
    print(x, end=' ')
```



## try/except/finally 捕捉异常

![img](try_except_else_finally-1804808.png)

```python
try:
    runoob()
except AssertionError as error:
    print(error)
else:
    try:
        with open('file.log') as file:
            read_data = file.read()
    except FileNotFoundError as fnf_error:
        print(fnf_error)
finally:
    print('这句话，无论异常是否发生都会执行。')
```



## assert 调试检查

![img](assert-1805161.png)

```python
# assert 条件为false时执行
x = 1
y = 2
assert x > y, 'x小一些'
```

