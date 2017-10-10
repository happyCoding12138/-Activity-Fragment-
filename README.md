# 一Activity多Fragment沉浸式-

1.在styles文件中定义BaseTheme主题，设置无标题属性，如下:\n
\t``<style name="BaseTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <item name="windowActionBar">false</item>
        <item name="windowNoTitle">true</item>``\n
\t添加MyTheme主题，继承BaseTheme主题，将MyTheme主题设置给activity
2.给fragment布局文件中的toolbar加上属性：``android:fitsSystemWindows="true"``
3.添加android版本号为19的styles文件，添加BaseTheme主题，如下：\n
\t``<style name="MyTheme" parent="BaseTheme">
        <item name="android:windowTranslucentStatus">true</item>
        <item name="android:windowTranslucentNavigation">true</item>
    </style>``\n
4.添加android版本号为21的styles文件，添加BaseTheme主题，如下：\n
``<style name="MyTheme" parent="BaseTheme">
        <item name="android:windowTranslucentStatus">false</item>
        <item name="android:windowTranslucentNavigation">true</item>
        <!--Android 5.x开始需要把颜色设置透明，否则导航栏会呈现系统默认的浅灰色-->
        <item name="android:statusBarColor">@android:color/transparent</item>
    </style>``
