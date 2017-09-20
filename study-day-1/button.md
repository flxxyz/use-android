## 几个按钮

### activity_button.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="15dp">

    <Button
        android:id="@+id/btn_1"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:text="按钮1"
        android:textSize="20sp"
        android:textColor="#fff"
        android:background="#06f"/>

    <Button
        android:id="@+id/btn_2"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:text="按钮2"
        android:textSize="20sp"
        android:textColor="#fff"
        android:background="@drawable/bg_btn2"
        android:layout_below="@id/btn_1"
        android:layout_marginTop="10dp" />

    <Button
        android:id="@+id/btn_3"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:text="按钮3"
        android:textSize="20sp"
        android:textColor="#f90"
        android:background="@drawable/bg_btn3"
        android:layout_below="@id/btn_2"
        android:layout_marginTop="10dp" />

    <Button
        android:id="@+id/btn_4"
        android:layout_width="match_parent"
        android:layout_height="40dp"
        android:text="按钮4"
        android:textSize="20sp"
        android:textColor="#fff"
        android:onClick="showToast"
        android:background="@drawable/bg_btn4"
        android:layout_below="@id/btn_3"
        android:layout_marginTop="10dp" />
</RelativeLayout>
```

### ButtonActivity.java
```
package com.udwbu.demo.test.helloworld;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.Toast;

public class ButtonActivity extends AppCompatActivity {

    private Button mBtn3;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_button);
        mBtn3 = (Button) findViewById(R.id.btn_button);
        mBtn3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast.makeText(ButtonActivity.this, "点击一下，点击一下", Toast.LENGTH_SHORT).show();
            }
        });
    }

    public void showToast(View view) {
        Toast.makeText(this, "点击一下，点击一下", Toast.LENGTH_SHORT).show();
    }
}
```

### bg_btn2.xml
```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <solid
        android:color="#f90"/>

    <corners
        android:radius="8dp"/>
</shape>
```

### bg_btn3.xml
```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <stroke
        android:width="1dp"
        android:color="#f90"/>

    <corners
        android:radius="8dp"/>
</shape>
```

### bg_btn4.xml
```
<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item
        android:state_pressed="true">
        <shape>
            <solid android:color="#cc7a00" />
            <corners android:radius="8dp" />
        </shape>
    </item>

    <item
        android:state_pressed="false">
        <shape>
            <solid android:color="#f90" />
            <corners android:radius="8dp" />
        </shape>
    </item>
</selector>
```