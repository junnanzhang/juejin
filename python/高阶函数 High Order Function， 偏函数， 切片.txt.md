# 高阶函数 High Order Function， 偏函数， 切片
#python

```
abs 内置函数，获取绝对值

sorted 内置函数，可以给列表排序

sorted(list, key=abs)
第二个参数接受一个函数， 用于排序

filter(a, b)
a为处理函数， b为处理的list
filter 比较诡异的是，返回的是filter 对象， 可以用list转换下

map(a, b) 和 filter 类似，返回的是map对象

reduce(a, b) 和map 类似  a函数会传入两个参数，前一个和 后一个

pathon3 中 reduce 使用需要引入

from functools import reduce

lambda 表达式

sorted(list, key=lambda x : x[1])  //x为元组，使用第二个元素排序

```

**偏函数**

[image:BAB84914-D3EE-4AE4-9E0F-84B1C1B2BE79-2529-000216D85CCE2F3F/255D4BAE-556B-4ABA-9F00-BD1AE6568D28.png]

列表可以切片
newLetters = letters[:]  //如此操作可以复制一个列表，简单
