 ##MIDWORK_NotePad     
 一.实现的功能
1.NoteList界面中笔记条目增加时间戳显示；
2.添加笔记查询功能（根据标题查询）；
3.UI美化
4.更改记事本的背景
二.项目结构（Java包和资源文件）

--> ![image](https://github.com/user-attachments/assets/57b3a5f1-ef54-4750-8b38-b6520a2e9c00)


--> ![image](https://github.com/user-attachments/assets/4da7e54e-1efb-447d-9fe6-d69bdef5df71)

三：效果概览：















四.功能以及效果演示
1.NotesList中显示条目增加时间戳显示
修改NoteEditor.java中updateNote方法，获取当前系统时间
增加一个textview组件

修改适配器内容
final String[] dataColumns = { NotePad.Notes.COLUMN_NAME_TITLE , NotePad.Notes.COLUMN_NAME_MODIFICATION_DATE} ; int[] viewIDs = { android.R.id.text1, R.id.text2};

NotesList.java中PROJECTION增加NotePad.Notes.COLUMN_NAME_MODIFICATION_DATE,

效果：


2.笔记查询（标题查询）
list_options_menu.xml添加menu_search

新建note_search.xml

AndroidManifest.xml注册NoteSearch
<activity android:name=".NoteSearch" android:label="@string/search_note" android:theme="@style/AppTheme"/>


新建NoteSearch.java功能



NotesList.java调用一下该方法

功能演示：



3.更改记事本的背景
新建styles.xml文件，下载背景图片并存入res,styles文件将图片设置为背景



在 AndroidManifest.xml 中的各个activity引用这个主题


效果：




4.UI美化
下载图片并存入res




引用并修改background属性，在notelistitem中
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:paddingLeft="6dip"
    android:paddingRight="6dip"
    android:paddingBottom="3dip"
    android:background="@drawable/bq2">




效果：

