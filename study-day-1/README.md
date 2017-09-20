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
