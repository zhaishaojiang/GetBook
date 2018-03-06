# Safari 手机自带键盘的搜索事件

HTML 代码

```HTML
<form id="myform" action="">
  <input id="searchIpt" type="search" />
</form>
```

JavaScript 代码

```
<script type="text/javascript">
  // 这里使用了jQuery插件
  $("#myform").bind('search', function () {
    alert('search')
  }
</script>
```



