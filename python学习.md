
# 基础知识
1. python使用a.b()，a表示变量,b()表示操作
2. #  被用来注释
3. input输入

# 与c差异
1. 字符串
	1. 可以使用加号合并字符串
	2. 可以用upper(),lower()直接转换大小写
	3. 使用rstrip()暂时删除空白
	4. 使用str()将其他量转化为字符串
2. 列表
	1. 使用负数索引
	2. 直接转化为列表**list()**
	3. 列表解析：方括号中一个计算式，一个为计算式提供值的语句
		`valve=[i**2 for i in range(1,10)]`
	列表的操作
	1. 末尾添加append
	2. 切片[:]
	3. 复制a=b[:],切片表示法表示创建副本
	4. 插入insert(位置，元素)
	5. 删除**del**名称，位置，remove,删除不知道名称的
	6. 弹出pop删除，并返回删除元素
	7. 排序sort,加参数reverse=Ture可翻转
	8. 临时排序**sorted()**
	9. 翻转**reverse()**
	10. 长度**len()**
3. 循环
	1. for a in b:
	2. for a in range(b,c):
	3. range(起始，结束，步长)
4. 判断
	1. 是否存在in
	2. 使用and not 
5. 字典
	1. 使用字典： c{a:b}->c[a]->b
	2. 遍历：for a,b in dictionary.items(), keys,valves进行遍历
6. 函数
	1. 关键值 `def a(x,y)  a(y=1,x=2)`
	2. 默认`def a(x=1,y=2)`
	3. 任意数量实参：`def a(*x)` \*代表创建空元组
	4.  \* \** 代表字典
	5. 导入类似c,使用函数类似a.b(),或者from 模块 import 函数 as 别名
	6. import apple as a; a.work()
	7. 快捷使用 from 模块 import \* 表示引入模块中所有函数，可直接使用
7. 类
	1. 使用：初始化：`def _init_(self)`
	2. 类的具体叫实例，类的函数叫方法
	3. 方法必须加self作为第一参数
	4. 类的继承：`def _init_(self,a,b,c)`:
					`super()._init_(a,b,c)`
8. 文件
	1. `with open('work.txt') as in` 
	2. 读取 使用 read()返回整个文件内容，使用readlines()返回按行分开的列表
	3. 替换replace(a,b)
	4. 写入`open(test.txt,'w')` as f 加 `f.write("abc")`,附加模式为`'a'`
9. 存储数据
	1. 存储json.dump(要存储的数据，存储对象)
	2. 加载json.load(存储对象)
	3. 需要引入json模块
10. 测试
	1. 需要引入unittest模块
	2. 例子
		~~~
		import unittest
		from test_fuction import get_name
		class nameTestCase(unittest.TestCase):
		    def test_FirstLastName(self):
		        fullname=get_name("wang","haoran")
		        self.assertEqual(fullname,"wanghaoran")#断言结果
		unittest.main()
		~~~
	3. 断言语句：assert...
# 拓展知识
1. 在命令板使用pip install xxx安装对应的包
2. 数学
	1. 引入math宏包
	2. 取对数`math.log10()`
	3. 