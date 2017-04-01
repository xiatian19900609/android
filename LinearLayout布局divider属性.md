# 设置LinearLayout布局子控件之间的分割线
##### 设置divider 、showDividers 属性
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:divider="@drawable/horizontal_divider"
    android:orientation="vertical"
    android:showDividers="middle">
</LinearLayout>
```
##### 自定义shape: height-横向 width-纵向  horizontal_divider.xml 
```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">

    <size android:height="0.5dp"/>
    <solid android:color="#cccccc"/>
</shape>
``` 