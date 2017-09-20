# 安卓自学第一天

## 什么是包名？

包名的由来是约定俗成的，继承自Java，是应用的唯一标识，为了避免和其它应用产生冲突。

名字大多都是域名反转 `helloworld.udwbu.com => com.udwbu.helloword`

> 一个简单的包名如下
> com.udwbu.helloworld

com 组织类型

udwbu 组织名

helloworld 产品名称



- - - -

## 实用性单词属性说明

``
LinearLayout // 流式布局
``

### 平分框内空间
```
<LinearLayout
        android:layout_width="match_parent"
        android:layout_height="200dp">

        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#b35151"></View>

        <View
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:background="#abcdef"></View>
    </LinearLayout>
```
