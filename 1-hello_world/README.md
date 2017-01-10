## 一、引入vue库

``` html
<script type="text/javascript" src="http://cdn.bootcss.com/vue/2.1.8/vue.js"></script>
```

## 二、页面功能

实现一个简单的页面功能：初始页面展示Hello Vue。

### 1. html内容

主要页面内容如下：

``` html
<div id="app">
  <h2>{{content}}</h2>
</div>
```

### 2. js内容

``` javascript
var app = new Vue({
  el: '#app',
  data: {
    content: 'Hello Vue!'
  }
})
```

### 3. 分析

测试了一下，将js内容放在head里或者放在页面内容之前，页面会显示{{content}}。需要将js内容放在页面内容后面，页面才会显示"Hello Vue!"。

由此可见，vuejs在执行页面渲染，进行数据与DOM绑定时，对应的页面元素必须已经加载。

## 三、完整代码

``` html
<!DOCTYPE html>
<html>

<head>
  <title>Hello World</title>
  <script type="text/javascript" src="http://cdn.bootcss.com/vue/2.1.8/vue.js"></script>
</head>

<body>
  <div id="app">
    <h2>{{content}}</h2>
  </div>

  <script type="text/javascript">
  var app = new Vue({
    el: '#app',
    data: {
      content: 'Hello Vue!'
    }
  })
  </script>
</body>

</html>
```

