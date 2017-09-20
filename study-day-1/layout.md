
### 混合布局

> 线性+相对
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context="com.udwbu.demo.test.helloworld.MainActivity">

    <View
        android:id="@+id/view_1"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:background="#000" />

    <View
        android:id="@+id/view_2"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:layout_below="@+id/view_1"
        android:layout_toRightOf="@+id/view_1"
        android:background="#ea2" />

    <LinearLayout
        android:id="@+id/ll_1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_below="@+id/view_2"
        android:background="#abcdef"
        android:orientation="horizontal"
        android:padding="10dp">

        <RelativeLayout
            android:id="@+id/ll_rl_1"
            android:layout_width="100dp"
            android:layout_height="match_parent"
            android:background="#c1b2"
            android:gravity="center"
            android:orientation="vertical">

            <View
                android:id="@+id/ll_rl_view_1_1"
                android:layout_width="20dp"
                android:layout_height="20dp"
                android:background="#000" />

            <View
                android:id="@+id/ll_view_1_2"
                android:layout_width="20dp"
                android:layout_height="20dp"
                android:layout_toRightOf="@+id/ll_rl_view_1_1"
                android:background="#fff" />

        </RelativeLayout>


        <RelativeLayout
            android:id="@+id/ll_rl_2"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_gravity="left"
            android:background="#b15269"
            android:padding="30dp">

            <View
                android:id="@+id/ll_rl_view_2_1"
                android:layout_width="100dp"
                android:layout_height="match_parent"
                android:background="#000" />

            <View
                android:id="@+id/ll_rl_view_2_2"
                android:layout_width="100dp"
                android:layout_height="match_parent"
                android:layout_marginLeft="10dp"
                android:layout_toRightOf="@+id/ll_rl_view_2_1"
                android:background="#fff" />
        </RelativeLayout>
    </LinearLayout>
</RelativeLayout>
```