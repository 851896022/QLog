# QLog
## 介绍
将qDebug、qWarning、qCritical、qFatal输出流重定向。同时输出到文件和调试窗口。
## 使用
在main函数中添加如下代码：
	qInstallMessageHandler(QLog::messageHandler);
## 备注
 Release版本的输出却没有文件信息、行数等信息。原因是：文件信息、行数等信息在Release版本默认舍弃。需要要在.pro文件定义一个宏
	DEFINES += QT_MESSAGELOGCONTEXT
