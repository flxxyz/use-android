# 安卓自学第三天

今天RadioButton, CheckBox, ImageView

一般加载网络图片都是使用第三方库来操作

这里我使用的是glide

自己初次写发现加载网络图片还需要用到权限，初学者注意啦(敲黑板 咚咚)

`项目下/src/main/AndroidMainifest.xml`里添加
```
<uses-permission android:name="android.permission.INTERNET" />
```
声明需要使用网络权限


## 实用性单词属性说明

gravity 位置

button 控制button原始样式

state_checked 选中状态


### 监听点击事件提取单独类
```
private Button mBtnTextView, mBtnButton, mBtnEditText, mBtnRadioBtn;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    mBtnTextView = (Button) findViewById(R.id.btn_textview);
    mBtnButton = (Button) findViewById(R.id.btn_button);
    mBtnEditText = (Button) findViewById(R.id.btn_edittext);
    mBtnRadioBtn = (Button) findViewById(R.id.btn_radiobtn);
    setListeners();  // 启动几个按钮的监听
}

private void setListeners() {
    OnClick onClick = new OnClick();  // 实例化OnClick类
    mBtnTextView.setOnClickListener(onClick);
    mBtnButton.setOnClickListener(onClick);
    mBtnEditText.setOnClickListener(onClick);
    mBtnRadioBtn.setOnClickListener(onClick);
}

private class OnClick implements View.OnClickListener {
    @Override
    public void onClick(View view) {
        Intent intent = null;
        switch (view.getId()) {
            case R.id.btn_textview:
                // 跳转到TextView演示界面
                intent = new Intent(MainActivity.this, TextViewActivity.class);
                break;
            case R.id.btn_button:
                // 跳转到Button演示界面
                intent = new Intent(MainActivity.this, ButtonActivity.class);
                break;
            case R.id.btn_edittext:
                // 跳转到EditText演示界面
                intent = new Intent(MainActivity.this, EditTextActivity.class);
                break;
            case R.id.btn_radiobtn:
                // 跳转到Button演示界面
                intent = new Intent(MainActivity.this, RadioButtonActivity.class);
                break;
        }
        startActivity(intent);
    }
}
```
