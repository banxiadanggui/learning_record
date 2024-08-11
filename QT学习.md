qt学习是[[机器人队事项]]的一部分，但似乎需要使用qml
___
# 基础认知
qt是用来开发嵌入式和普通电脑程序界面所使用的工具，优点是不同平台能够通用，底层为c++

---
# 基础操作

开始一个qt项目
选择开发工具使用qmaker
details中选择基类
	1. qwidget是基类，qmainwindow和qdialog是主类
新建好后系统会自动生成项目文件
	1. 后缀为.pro的是qt的项目文件
	2. 后缀为.ui的是qtui的文件

pro文件解析
	~~~
	QT       += core gui(使用官方的两个模块)
	
	greaterThan(QT_MAJOR_VERSION, 4): QT += widgets
	
	CONFIG += c++17
	
	# You can make your code fail to compile if it uses deprecated APIs.
	# In order to do so, uncomment the following line.
	#DEFINES += QT_DISABLE_DEPRECATED_BEFORE=0x060000    # disables all the APIs deprecated before Qt 6.0.0
	
	SOURCES += \ (指定源文件)
	    main.cpp \
	    mywindow.cpp
	
	HEADERS += \
	    mywindow.h
	
	FORMS += \(指定ui文件)
	    mywindow.ui
	
	# Default rules for deployment.
	qnx: target.path = /tmp/$${TARGET}/bin
	else: unix:!android: target.path = /opt/$${TARGET}/bin
	!isEmpty(target.path): INSTALLS += target
	
	~~~
	具体使用文件参考笔记
# 基本语法
1.  QApplication 是qy框架提供的应用程序类，负责qt事件的处理
2. `return a.exec()`调用方法，程序阻塞
3. `Mywindow w`创建自己的窗口对象
4. `w.show()`调用方法将窗口展示出来
5. 按钮的属性可在右下角修改
6. 修改按钮的文本：在mywindow.cpp里，ui.setupUi(this)中使用ui->按钮名->setText("启动")
# 底层知识
1. main.cpp如何编译成可执行文件？`g++ -o main mian.cpp`
2. makefile文件最终决定以怎样的顺序编译多个源文件，写好后只用执行make命令
3. qmake会根据pro文件的内容自动生成makefile
4. 进行操作会触发事件并发出信号，信号是只需声明，无需实现的的函数
5. 槽就是槽函数，也铜鼓同样的方法进行查询
6. 槽和信号连接需要使用connect函数进行连接
7. `connect(ui->btnMax,SIGNAL(clicked()),this,SLOT(showMaximised()));`
8. qt快捷键`ctrl+alt+up/down`