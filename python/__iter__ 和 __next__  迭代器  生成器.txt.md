#  __iter__ 和 __next__  迭代器  生成器
#python


[image:6137CCA7-35DB-430A-9345-9EF23CF824F7-2529-000207F06DBE4E8E/20B9B014-0FCC-4AE7-AC51-1A059019435C.png]

Iter方法生成迭代器，next到最后一个会抛出异常
[image:32E85CE4-CE1C-4E86-95D0-C28F8EE9077D-2529-0002176E7D606385/0297E413-6240-479B-82C0-0EA8162E1775.png]

**生成器**
生成器首先是一个迭代器，和迭代器一样只能被遍历迭代一次，每迭代一次只能生成一个元素，动态生成的，不在内存中，优点是节约内存

和迭代器不同， 创建方式不同
有自己特殊的方法
[image:21A0AC1E-3976-4E1D-BBB6-7D6D1C57FFF0-2529-000219DCD94A410A/D06C3BC7-42E7-4F92-958F-F8F98775344A.png]

yield 编写生成器
yield 的使用方法和 return 类似。不同的是，return 可以返回有效的 Python 对象，而 yield 返回的是一个生成器，函数碰到 return 就直接返回了，而使用了 yield 的函数，到 yield 返回一个元素，当再次迭代生成器时，会从 yield 后面继续执行，直到遇到下一个 yield 或者函数结束退出。
[image:3C114BBD-FEEB-4D21-9F2A-2DF3ED43E089-2529-00021A1FB6B4D892/39D783BB-4053-4B8C-8ABE-0E4812CA66F5.png]

