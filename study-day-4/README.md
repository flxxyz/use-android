# 安卓自学第四天

使用ListView写写小新闻信息列表页

需要用到的组件与技术
- Java基本语法
- Adapter
- Toast
- TextView (component)
- LinearLayout (component)
- ImageView (component)
- setOnItemClickListener (action)
- setOnItemLongClickListener (action)
- glide (package)

- - - -

测试通过
![123](/study-day-4/test-pic.png)
ov系统不兼容，反正我也不会适配┑(￣Д ￣)┍


- - - -
`项目下/src/main/values/colors.xml`添加颜色标签
```
<color name="colorWhite">#ffffff</color>
```

组件内定义点击选择悬浮的状态操作
```
<item android:state_focused="true"
    android:drawable="@color/colorGrayLight"/>
```