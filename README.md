# Face_recognition_CSIC
基于pycharm+MySQL+python+pyqt5设计和实现的人脸识别考勤管理系统

一、项目概述
基于pycharm+MySQL+python+pyqt5设计和实现的人脸识别考勤管理系统，系统主要
功能包括：
（1）人脸识别；
（2）UI可视化；
（3）实时监控显示与数据存储；
（4）人脸识别数据管理及查询。

二、配置说明
1、软件配置
（1）Windows10 x64操作系统；
（2）python3.6；
（3）PyCharm Community Edition with Anaconda plugin 2020.1.2；
（4）Anaconda3-5.2.0-Windows-x86_64；
（5）TensorFlow-gpu 1.14.0；
（6）PyQt5 5.9.2；
（7）MySQL8.0;
（8）CUDA 10.0;
（9）CUDNN 7.4.1；
（10）Navicat Premium 12；
（11）numpy 1.14.2；
（12）PySocks 1.6.8。
2、解释器
	有些库文件是在系统调试及使用时必须导入的，可以pip install 安装，也可以通过pycharm IDE导入。Python解释器如下所示：
 

三、系统代码解释
1、核心框架
 
2、人脸信息采集端
 
3、数据管理端
 
示例：
 
4、文件解释，如图所示：
（1）	attendance_csv文件夹包含的是签到表；
（2）	attendance_snapshot文件夹包含的是签到快照；
（3）	config文件夹包含的是配置文件
（4）	datasets文件夹包含的是人脸采集数据集；
（5）	dlib_128D_csv文件夹包含的是dlib特征提取训练后保存的模型；
（6）	haarcascades文件夹包含的是级联分类器文件，是opencv进行人脸识别的文件，具体还有其他的分类器，像识别眼睛嘴巴还有微笑什么的；
（7）	icons这个文件夹主要是存放UI页面的图标；
（8）	modules文件夹包含的是dlib特征提取模型；
（9）	recognizer文件夹包含的是人脸识别模型；
（10）	ui文件夹包含的UI设计文件；
（11）	core.py是核心框架代码模块，主要功能包括：人脸识别实时监控、签到表创建及存储、消息推送等；
（12）	dataRecord.py是人脸数据采集端代码模块，主要功能包括：员工信息增删改查、人才识别数据采集与存储、数据直接导入等；
（13）	dataManage.py是人脸数据管理端代码模块，主要功能包括：数据库查询、模型训练、用户管理等；
（14）	几个.dat模块为人脸识别系统的人脸标记、预测及识别网络。
 
5、数据库连接
core.py模块实时人脸识别显示的内容包括置信度打分、中文名、中文名拼音，识别成功后显示“已识别”，系统日志会同步显示“员工编号+员工姓名+已识别”信息，同时信息直接保存到数据库。本系统数据库为MySQL，可视化端使用Navicat Premium 12，数据库连接如下：
 
（1）host、port和password是在安装MySQL设置的，不可更改，如图：

 
 
（2） 根据上面显示的代码，创建数据库mytest，其中字符集是utf8，排序规则是utf8_general_ci，目的是中文字段显示。
 
（3）人脸识别考勤实时数据存储和导出如图所示：
 
 
 
