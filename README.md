jBootstrapPage
==============

一个Bootstrap风格的分页控件，对于喜欢Bootstrap简洁美观和扁平化的同学可以关注jBootstrapPage，
目前jBootstrapPage最新版为V0.1，后续还有更多功能需要完善。

demo演示地址: http://www.it175.cn/demo/jBootstrapPage/

代码示例:
===============
html代码

```html
<html>
<head>
	<link href="jBootsrapPage.css" rel="stylesheet" />
  <script src="jquery-1.10.2.min.js"></script>
  <script src="jBootstrapPage.js"></script>
</head>
<body>
	<div>
		<ul class="pagination"></ul>
	</div>
<body>
</html>
```

javascript代码调用
===============
每页显示多少条数据(pageSize),显示多少个分页按钮(buttons),传入数据总行数(total)即可，
如果需要在选中某一页，然后去请求服务器端，可以在onPageClicked回调函数中完成。
 
```javascript


<script type="text/javascript">
$(function(){
    createPage(10, 13, 150);
    
    function createPage(pageSize, buttons, total) {
        $(".pagination").jBootstrapPage({
            pageSize : pageSize,
            total : total,
            maxPageButton:buttons,
            onPageClicked: function(obj, pageIndex) {
                alert((pageIndex+1)+'页');
            }
        });
    }
});
</script>


```
