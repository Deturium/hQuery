# hQuery


## 自己实现的jQuery

- 参考jQuery的API设计

- 支持链式调用

- 只兼容高版本浏览器

- 还没有经过完整的测试


## 用法示例

```javascript
<script src='hQuery.js'></script>

<script>

let h = window.hQuery

h('#id li')
	.children(2)
	.find('.color')
	.next()
	.append('<div>dome</div>')
	.end()
	.css('font-size', '2em')
	.addClass('selected')
	.on('click', function () {
     	... 
	})

h.extend({
  "method1": func1,
  "method2": func2
})
	
</script>
```