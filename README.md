# Python-20-
 Python学习笔记(20)
# p65 字典的特点
d={'name':'张三'，'name':'李四'}  #key不允许重复，会出现值覆盖的情况
print(d)

d={'nmae':'张三','nickname':'张三'}  #value是可以重复的
print(d)  

lst=[10,20,30]
lst,insert(1,100)
print(lst)  #输出为:[10,100,20,30]
d={lst:100}
print(d)  #这里会弹出警告，lst为列表，是一个可变对象，是不允许去计算哈希值的

#字典会浪费较大的内存，是一个空间换时间的数据结构



# p66 字典生成式
#使用内置函数zip()来生成字典
items=['Fruits','Books','Others']
prices=[96,78,85]
d={item.upper()'这个是大写的内置函数':price   for item,price in zip(items,prices)}
print(d)
#如果key和value数量不一致，以元素少的那个为基准打印



# p67 什么是元组
#元组是Python内置的数据结构之一，是一个不可变序列
‘’‘不可变序列，可变序列’‘’
'''可变序列 列表 字典'''
lst=[10,20,45]
print(id(lst))
lst.append(300)
print(id(lst))  #内存地址没有发生更改

'''不可变序列：字符串，元组'''
s='hello'
print(id(s))
s=s+'world'
print(id(s))
print(s)  #这里的内存地址发生更改，所以是不可变序列

#列表使用[]定义，元组使用()去定义，他们使用的元素是相似的
