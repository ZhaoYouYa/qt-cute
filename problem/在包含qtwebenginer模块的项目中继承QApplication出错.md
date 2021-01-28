# [部分]

使用Qt版本为5.15.0,使用的C++编译器是msvc2019x64.

0. 我想要监听整个应用程序的事件。
1. 我继承了QApplication,然后重载函数bool notify(QObject*,   QEvent*)，以接收应用程序的事件。
2. 我的项目里使用了 qtwebenginer模块。
3. 可以编译成功。但是程序会出现崩溃的情况。
4. 并不是因为重载了notify函数，而是因为继承了QApplication
```cpp
#include <QApplication>
class MyApplication : public QApplication {
    Q_OBJECT
public:
    MyApplication(int &argc, char **argv):QApplication(argc,argv){}

} 
```
只实现这些，别的什么事情都不做，就导致程序奔溃。

5. 如果没有qtwebenginer模块，一切正常。


## 解决方法
我不知道具体的原因是什么，我猜测这是由于应用程序向chrome内核传递事件消息时除了问题，chrome内核通常是多进程的，在我的程序启动时，qtwebenginer.exe也被启动。我也没有办法解决，但是我发现我的需求并不是只能使用notify实现，我重载了bool QObject::event(QEvent*)实现了我的需求。 