# [����]

ʹ��Qt�汾Ϊ5.15.0,ʹ�õ�C++��������msvc2019x64.

0. ����Ҫ��������Ӧ�ó�����¼���
1. �Ҽ̳���QApplication,Ȼ�����غ���bool notify(QObject*,   QEvent*)���Խ���Ӧ�ó�����¼���
2. �ҵ���Ŀ��ʹ���� qtwebenginerģ�顣
3. ���Ա���ɹ������ǳ������ֱ����������
4. ��������Ϊ������notify������������Ϊ�̳���QApplication
```cpp
#include <QApplication>
class MyApplication : public QApplication {
    Q_OBJECT
public:
    MyApplication(int &argc, char **argv):QApplication(argc,argv){}

} 
```
ֻʵ����Щ�����ʲô���鶼�������͵��³�������

5. ���û��qtwebenginerģ�飬һ��������


## �������
�Ҳ�֪�������ԭ����ʲô���Ҳ²���������Ӧ�ó�����chrome�ں˴����¼���Ϣʱ�������⣬chrome�ں�ͨ���Ƕ���̵ģ����ҵĳ�������ʱ��qtwebenginer.exeҲ����������Ҳû�а취����������ҷ����ҵ����󲢲���ֻ��ʹ��notifyʵ�֣���������bool QObject::event(QEvent*)ʵ�����ҵ����� 