### MIDWORK_NotePad     
## 一.实现的功能
1.NoteList界面中笔记条目增加时间戳显示；
2.添加笔记查询功能（根据标题查询）；
3.UI美化
4.更改记事本的背景
##  二.项目结构（Java包和资源文件）

-->![image](https://github.com/user-attachments/assets/e2fe9378-81e7-403d-ad20-89644918da58)

 



-->![image](https://github.com/user-attachments/assets/a4446cae-c45e-428f-83de-155455ce893b)



##  三：效果概览：


![image](https://github.com/user-attachments/assets/9b5b4eaa-fc3b-454b-8cd2-545d4f0434cd)



![image](https://github.com/user-attachments/assets/8aa8dacb-8e56-4615-aed2-71805d4999cd)


![image](https://github.com/user-attachments/assets/3d7790db-30c3-4fd6-8d6a-b67587682442)



##  四.功能以及效果演示
#  1.NotesList中显示条目增加时间戳显示

修改NoteEditor.java中updateNote方法，获取当前系统时间

![image](https://github.com/user-attachments/assets/57f5bb9e-3e26-484b-bbe6-998bcc737c1b)

增加一个textview组件

![image](https://github.com/user-attachments/assets/01c4ea10-65da-4e49-a4e1-f335f90203cd)


修改适配器内容

final String[] dataColumns = { NotePad.Notes.COLUMN_NAME_TITLE , NotePad.Notes.COLUMN_NAME_MODIFICATION_DATE} ; int[] viewIDs = { android.R.id.text1, R.id.text2};

NotesList.java中PROJECTION增加NotePad.Notes.COLUMN_NAME_MODIFICATION_DATE,

效果：


![image](https://github.com/user-attachments/assets/f7b57cdf-717f-4c9e-9db7-0ffa8e278fcf)



#  2.笔记查询（标题查询）

list_options_menu.xml添加menu_search

![image](https://github.com/user-attachments/assets/6312af37-6905-4c65-8af7-598a4f730445)


新建note_search.xml

![image](https://github.com/user-attachments/assets/0242cced-97d1-4135-8e2b-8007ff28b7d5)


AndroidManifest.xml注册NoteSearch

<activity android:name=".NoteSearch" android:label="@string/search_note" android:theme="@style/AppTheme"/>


新建NoteSearch.java功能

![image](https://github.com/user-attachments/assets/c56d3b7d-e1d4-4bd7-98db-936d95120aa6)


NotesList.java调用一下该方法


![image](https://github.com/user-attachments/assets/86f47f02-1c02-462d-8652-ef78a74da8b5)


功能演示：

![image](https://github.com/user-attachments/assets/315e8493-50b5-4363-9a0d-d430eab32e8c)


#  3.更改记事本的背景
新建styles.xml文件，下载背景图片并存入res,styles文件将图片设置为背景

![image](https://github.com/user-attachments/assets/84875583-0ea8-47f8-8a6c-d5b05f9970ff)

![image](https://github.com/user-attachments/assets/e599ff6e-bfdd-473b-bb1e-6e3b44c7226b)


在 AndroidManifest.xml 中的各个activity引用这个主题

![image](https://github.com/user-attachments/assets/b0c4a5d7-9e71-4cb4-8f83-f2eaaf4c67ff)


效果：

![image](https://github.com/user-attachments/assets/b74f6f52-3181-486c-b929-22e581df0728)

![image](https://github.com/user-attachments/assets/3388e748-97e4-4e4c-84ce-de3f88d43d67)


#  4.UI美化
下载图片并存入res

![image](https://github.com/user-attachments/assets/43e59dc5-57c0-42dc-bb47-1b154687f2dd)



引用并修改background属性，在notelistitem中
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:paddingLeft="6dip"
    android:paddingRight="6dip"
    android:paddingBottom="3dip"
    android:background="@drawable/bq2">


![image](https://github.com/user-attachments/assets/e1e333be-81d6-4580-9a03-f381f363b699)

效果：


![image](https://github.com/user-attachments/assets/7641f45e-5ac5-4c5f-b4ca-67dbc6852fb6)





