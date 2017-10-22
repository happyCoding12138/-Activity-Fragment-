# 一Activity多Fragment沉浸式-

1.在styles文件中定义BaseTheme主题，设置无标题属性，如下:

    <style name="BaseTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <item name="windowActionBar">false</item>
        <item name="windowNoTitle">true</item>
    </style>
    
    添加MyTheme主题，继承BaseTheme主题，将MyTheme主题设置给activity
        
2.给fragment布局文件中的toolbar加上属性：``android:fitsSystemWindows="true"``

3.添加android版本号为19的styles文件，添加BaseTheme主题，如下：

    <style name="MyTheme" parent="BaseTheme">
        <item name="android:windowTranslucentStatus">true</item>
        <item name="android:windowTranslucentNavigation">true</item>
    </style>
    
4.添加android版本号为21的styles文件，添加BaseTheme主题，如下：

    <style name="MyTheme" parent="BaseTheme">
    
        <!--这个属性为true时，状态栏有一个遮盖的半透明效果，为false时，状态栏跟toolbar颜色一样-->
        <item name="android:windowTranslucentStatus">false</item>
        
        <!--这个属性为rue时，底部导航栏会遮盖布局，为false时，底部导航栏会把布局顶上去-->
        <item name="android:windowTranslucentNavigation">true</item>
        
        <!--不设置透明色，navigationBar的颜色会是纯黑的-->
        <item name="android:navigationBarColor">@android:color/transparent</item>
    </style>
    
