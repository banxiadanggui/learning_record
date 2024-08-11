[[机器人队事项]]需要使用

# 可变参数函数
参考网址[C语言可变函数参数 - 哔哩哔哩 (bilibili.com)](https://www.bilibili.com/read/cv20412768/)
1. 头文件`#include <stdarg.h>`
2. 主体为1个变量和三个函数
3. 变量为`va_list `,为地址指针
4. 初始化`va_start(va_list,最后一个已知参数)`,
5. 检索函数参数列表中下一个类型为type的参数`va_arg(va_list,type)`
6. 结束将地址指针指向NULL`va_end(va_list)`
7. 由于加长原则，type无法指定为float,参见[可变参数列表函数，参数为float类型时会读入错误以及解决方法_可变参数函数 打印错误-CSDN博客](https://blog.csdn.net/douyangyang/article/details/4041768?ops_request_misc=&request_id=&biz_id=102&utm_term=stdarg%20float&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-6-4041768.142^v100^pc_search_result_base8&spm=1018.2226.3001.4187)
8. 使用流程
	~~~
	该文件提供了实现可变参数功能的函数和宏。具体步骤如下：
	1.定义一个函数,最后一个参数为省略号(…),省略号前面可以设置自定义参数。
	2.在函数中创建一个 va_list 类型变量,该类型是在 stdarg.h 头文件中定义的。
	3.使用 int 参数和 va_start 宏来初始化 va_list 变量为一个参数列表。宏 va_start 是在 stdarg.h 头文件中定义的。
	4.使用 va_arg 宏和 va_list 变量来访问参数列表中的每个项。
	5.用宏 va_end 来清理赋予 va_list 变量的内存。
	~~~
## 类
参考[C++总结（三）——类与对象 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/619050568)
格式
~~~
class person
{
public:
	string name[10];
	...
}
~~~
语法
1. 继承方式`class 子类: 继承方式 基类`
2. 初始化
	~~~
	class Person 
	{
	  private:
	    string name;
	    int age;
	  public:
	    Person(string n, int a) 
	    {
	      name = n;
	      age = a;
	    }
	    //
	MyClass(int n, const std::string& s): num(n), str(s) {}
	~~~
3. 类的区别public公共访问，protect子类访问，private限制访问
4. 访问方式：跟python一样通过对象名访问
5. 静态成员：可被类的所有实例访问且可被直接使用类名进行访问
	1. 使用static
	2. 访问函数为`类名::函数名`
6. 销毁对象：类中的方法，在类名前加~
7. 