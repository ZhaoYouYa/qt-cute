
ʹ���κ�IDE�Ĺ�ע�ĵ㶼�ǲ��ġ�

��Ҫ֪����
1. �����������ĵ�ַ��ָ��ѡ�build���ͺ�Ŀ¼�ȵȡ�
2. ������������Ŀ¼��ѡ�
3. �����������Ҫ�������C++����ͷ�ļ��Ϳ��ļ�����C++ͨ����cmakeָ����ʹ��vsҲ��ָ������Ŀ¼��������Ŀ¼�������
4. �ı��༭����style,�������ͣ�������ɫ�ȵȡ�
5. ������������ʾ��
6. �ı�����淶��utf-8 ���ǣ�
7. һЩ���ܴ��ڵĴ򿪺͹رա�
8. ��ݼ���

���ϣ��Ϳ��Ի���������ʹ��һ��IDE�ˡ�Ŀǰ�ʹ�õ�IDE��Ҫ��vs��vscode��qtcreator��


ʹ��qtcreator��ʱ��Ĭ�ϵİ������汳��ɫ�ǰ�ɫ�ģ��е���ۣ�Ϊ�˿��Կ������һ�㣬�����ĳ���ɫ����ͼЧ����

![](images/greenqtcreator.PNG)

QtCreator����������û���ṩ�ı�����ĵ�����ɫ�Ĺ��ܣ����ǿ���ͨ������������QtCreator����ͬʱ���ݲ�������������Щ����ʹ��Qt ��stylesheet,����ʮ�����Ķ���,�����������õȵȡ���

1. ��windows��ʹ��powershell,�������ñ�����
```pwsh
PS C:\> $profile #�鿴profile�ĵ�ַ�����û�У����½�һ����
PS C:\> New-Item -Type file -Force $profile
```
2. �༭profile�ļ�
```
function qt {
	 E:\Qt\Tools\QtCreator\bin\qtcreator.exe --stylesheet E:\Qt\qtcreatorstyle.txt
}
```
����·����һ����Qtcreator.exe��·����һ�����Զ����qss��·������qtcreatorstyle.txt������ȫ��qss���﷨��

```css
QPlainTextEdit
{
background-color: rgb(199, 237, 204);
}
QTextEdit
{
background-color: rgb(199, 237, 204);
}
```
3. Ȼ������powershell�Ϳ��Լ��� qt������QtCreator�ˡ�
4. ʹ�������л���ʮ�ַ���ģ������Ȼ��ʹ��˫��ͼ��ķ�ʽ��QtCreator,�Ͳ���Ҫ����������powershell�ˣ�ֱ������QtCreator�Ŀ�ݷ�ʽ�Ϳ����ˡ�


![](images/qtcreatorlink.PNG)