# 安卓自学第二天

## 实用性单词属性说明

EditText

hint


### 监听文本框中内容变化
```
.addTextChangedListener(new TextWatcher() {
    @Override
    public void beforeTextChanged(CharSequence charSequence, int i, int i1, int i2) {
        // 编辑框内文字改变前
    }

    @Override
    public void onTextChanged(CharSequence charSequence, int i, int i1, int i2) {
        // 编辑框内文字改变进行中
    }

    @Override
    public void afterTextChanged(Editable editable) {
        // 编辑框内文字改变后
    }
});
```


### Log 打印报错信息与日志
```
Log.d("edittext", "1234567890);
```