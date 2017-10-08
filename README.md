# hQuery

## 自己实现的jQuery

- 参考jQuery的API设计

- 支持链式调用

- 只兼容高版本浏览器

- 未经完整测试


# 文档

<a name="hQuery"></a>

## hQuery
**Kind**: global class  

* [hQuery](#hQuery)
    * [new hQuery(selector, [context])](#new_hQuery_new)
    * _instance_
        * [.find(selector)](#hQuery+find) ⇒ [<code>hQuery</code>](#hQuery)
        * [.first()](#hQuery+first) ⇒ [<code>hQuery</code>](#hQuery)
        * [.last()](#hQuery+last) ⇒ [<code>hQuery</code>](#hQuery)
        * [.eq(num)](#hQuery+eq) ⇒ [<code>hQuery</code>](#hQuery)
        * [.parent()](#hQuery+parent) ⇒ [<code>hQuery</code>](#hQuery)
        * [.children([num])](#hQuery+children) ⇒ [<code>hQuery</code>](#hQuery)
        * [.next()](#hQuery+next) ⇒ [<code>hQuery</code>](#hQuery)
        * [.prev()](#hQuery+prev) ⇒ [<code>hQuery</code>](#hQuery)
        * [.slice(start, end)](#hQuery+slice) ⇒ [<code>hQuery</code>](#hQuery)
        * [.filter(fn)](#hQuery+filter) ⇒ [<code>hQuery</code>](#hQuery)
        * [.end()](#hQuery+end) ⇒ [<code>hQuery</code>](#hQuery)
        * [.html([html])](#hQuery+html) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
        * [.text([text])](#hQuery+text) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
        * [.val([value])](#hQuery+val) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
        * [.attr(attr, [value])](#hQuery+attr) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
        * [.append(html)](#hQuery+append) ⇒ [<code>hQuery</code>](#hQuery)
        * [.prepend(html)](#hQuery+prepend) ⇒ [<code>hQuery</code>](#hQuery)
        * [.remove()](#hQuery+remove) ⇒ [<code>hQuery</code>](#hQuery)
        * [.replaceWith(html)](#hQuery+replaceWith) ⇒ [<code>hQuery</code>](#hQuery)
        * [.hide()](#hQuery+hide) ⇒ [<code>hQuery</code>](#hQuery)
        * [.show()](#hQuery+show) ⇒ [<code>hQuery</code>](#hQuery)
        * [.toggle()](#hQuery+toggle) ⇒ [<code>hQuery</code>](#hQuery)
        * [.css(attr, [value])](#hQuery+css) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
        * [.hasClass(className)](#hQuery+hasClass) ⇒ <code>boolean</code>
        * [.addClass(className)](#hQuery+addClass) ⇒ [<code>hQuery</code>](#hQuery)
        * [.removeClass(className)](#hQuery+removeClass) ⇒ [<code>hQuery</code>](#hQuery)
        * [.toggleClass(className, [force])](#hQuery+toggleClass) ⇒ [<code>hQuery</code>](#hQuery)
        * [.on(event, handler)](#hQuery+on) ⇒ [<code>hQuery</code>](#hQuery)
        * [.off(event, handler)](#hQuery+off) ⇒ [<code>hQuery</code>](#hQuery)
        * [.one(event, handler)](#hQuery+one) ⇒ [<code>hQuery</code>](#hQuery)
        * [.each(fn)](#hQuery+each) ⇒ [<code>hQuery</code>](#hQuery)
    * _static_
        * [.extend(name, fn)](#hQuery.extend)
        * [.get(url, callback)](#hQuery.get)
        * [.post(url, data, callback)](#hQuery.post)

<a name="new_hQuery_new"></a>

### new hQuery(selector, [context])
hQuery构造函数，可以直接h()调用

**Returns**: [<code>hQuery</code>](#hQuery) - - hQuery对象  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| selector | <code>String</code> \| <code>DOM</code> |  | querySelectAll的选择器 |
| [context] | <code>DOM</code> | <code>document</code> | 选择器的根节点 |

<a name="hQuery+find"></a>

### hQuery.find(selector) ⇒ [<code>hQuery</code>](#hQuery)
以当前对象的第一个节点为根节点，返回符合选择器的子节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuey对象  

| Param | Type | Description |
| --- | --- | --- |
| selector | <code>string</code> | 选择器 |

<a name="hQuery+first"></a>

### hQuery.first() ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中的第一个节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuey对象  
<a name="hQuery+last"></a>

### hQuery.last() ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中的最后一个节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  
<a name="hQuery+eq"></a>

### hQuery.eq(num) ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中的第n个节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| num | <code>number</code> | 从0开始指定第num个节点，可接受负数 |

<a name="hQuery+parent"></a>

### hQuery.parent() ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中每一个节点的父节点集合

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  
<a name="hQuery+children"></a>

### hQuery.children([num]) ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中第一个节点的直接子节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| [num] | <code>number</code> | 指定第几个子节点 |

<a name="hQuery+next"></a>

### hQuery.next() ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中所有节点的下一个兄弟节点的集合

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  
<a name="hQuery+prev"></a>

### hQuery.prev() ⇒ [<code>hQuery</code>](#hQuery)
返回hQuery对象中所有节点的上一个兄弟节点的集合

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  
<a name="hQuery+slice"></a>

### hQuery.slice(start, end) ⇒ [<code>hQuery</code>](#hQuery)
返回[start, end)的节点集合

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| start | <code>number</code> | 起点 |
| end | <code>number</code> | 终点 |

<a name="hQuery+filter"></a>

### hQuery.filter(fn) ⇒ [<code>hQuery</code>](#hQuery)
返回满足筛选函数的节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| fn | <code>function</code> | 用作筛选的函数，应返回boolean值 |

<a name="hQuery+end"></a>

### hQuery.end() ⇒ [<code>hQuery</code>](#hQuery)
回溯到链上的上一个hQuery对象

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - 全新的hQuery对象  
**Example**  
```js
h('#id').find('.class').end() // 会被回溯到h('#id')
```
<a name="hQuery+html"></a>

### hQuery.html([html]) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
返回或者设置节点的html

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: <code>string</code> \| [<code>hQuery</code>](#hQuery) - - 返回html内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [html] | <code>string</code> | 要设置的html |

<a name="hQuery+text"></a>

### hQuery.text([text]) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
返回或者设置节点的text

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: <code>string</code> \| [<code>hQuery</code>](#hQuery) - - 返回text内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [text] | <code>string</code> | 将要设置的text值 |

<a name="hQuery+val"></a>

### hQuery.val([value]) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
返回或者设置节点的value

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: <code>string</code> \| [<code>hQuery</code>](#hQuery) - - 返回value内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [value] | <code>string</code> | 要设置的value |

<a name="hQuery+attr"></a>

### hQuery.attr(attr, [value]) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
返回或者设置节点的属性

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: <code>string</code> \| [<code>hQuery</code>](#hQuery) - - 返回属性值或者自身  

| Param | Type | Description |
| --- | --- | --- |
| attr | <code>string</code> \| <code>object</code> | 想取得或者将要设置的attr值，可传入{ attr: value }的对象 |
| [value] | <code>string</code> | 要设置的attr值 |

<a name="hQuery+append"></a>

### hQuery.append(html) ⇒ [<code>hQuery</code>](#hQuery)
在节点的子节点末尾添加html

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 要添加的html或者节点，DOM可传入多个 |

<a name="hQuery+prepend"></a>

### hQuery.prepend(html) ⇒ [<code>hQuery</code>](#hQuery)
在节点的子节点开头添加html

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 要添加的html或者节点，DOM可传入多个 |

<a name="hQuery+remove"></a>

### hQuery.remove() ⇒ [<code>hQuery</code>](#hQuery)
删除所有节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  
<a name="hQuery+replaceWith"></a>

### hQuery.replaceWith(html) ⇒ [<code>hQuery</code>](#hQuery)
替代当前节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 用以替换的html或者DOM，DOM可传入多个 |

<a name="hQuery+hide"></a>

### hQuery.hide() ⇒ [<code>hQuery</code>](#hQuery)
隐藏节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  
<a name="hQuery+show"></a>

### hQuery.show() ⇒ [<code>hQuery</code>](#hQuery)
显示节点

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  
<a name="hQuery+toggle"></a>

### hQuery.toggle() ⇒ [<code>hQuery</code>](#hQuery)
切换隐藏和显示的状态

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  
<a name="hQuery+css"></a>

### hQuery.css(attr, [value]) ⇒ <code>string</code> \| [<code>hQuery</code>](#hQuery)
返回或者设置节点的css

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: <code>string</code> \| [<code>hQuery</code>](#hQuery) - - 返回属性值或者自身  

| Param | Type | Description |
| --- | --- | --- |
| attr | <code>string</code> \| <code>object</code> | 取得或者将要设置的css值，可传入{ attr: value }的对象 |
| [value] | <code>string</code> | 要设置的css值 |

<a name="hQuery+hasClass"></a>

### hQuery.hasClass(className) ⇒ <code>boolean</code>
检测节点是否有该class

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 检测的类名 |

<a name="hQuery+addClass"></a>

### hQuery.addClass(className) ⇒ [<code>hQuery</code>](#hQuery)
为节点添加class

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 增加的类名 |

<a name="hQuery+removeClass"></a>

### hQuery.removeClass(className) ⇒ [<code>hQuery</code>](#hQuery)
为节点去除class

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 去除的类名 |

<a name="hQuery+toggleClass"></a>

### hQuery.toggleClass(className, [force]) ⇒ [<code>hQuery</code>](#hQuery)
切换class

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 切换的类名 |
| [force] | <code>boolen</code> | 可选切换方式，true表示增加，false表示去除 |

<a name="hQuery+on"></a>

### hQuery.on(event, handler) ⇒ [<code>hQuery</code>](#hQuery)
增加绑定事件

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数，记得处理this绑定 |

<a name="hQuery+off"></a>

### hQuery.off(event, handler) ⇒ [<code>hQuery</code>](#hQuery)
去除绑定事件

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数 |

<a name="hQuery+one"></a>

### hQuery.one(event, handler) ⇒ [<code>hQuery</code>](#hQuery)
增加绑定事件，该事件在触发一次后会被移除

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数，记得处理this绑定 |

<a name="hQuery+each"></a>

### hQuery.each(fn) ⇒ [<code>hQuery</code>](#hQuery)
对每一个节点调用处理函数

**Kind**: instance method of [<code>hQuery</code>](#hQuery)  
**Returns**: [<code>hQuery</code>](#hQuery) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| fn | <code>function</code> | 处理函数，如果返回false会中断后续执行 |

<a name="hQuery.extend"></a>

### hQuery.extend(name, fn)
在hQuery的原型链上扩展新的方法

**Kind**: static method of [<code>hQuery</code>](#hQuery)  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>name</code> | 新增的方法名 |
| fn | <code>function</code> | 新增的方法 |

<a name="hQuery.get"></a>

### hQuery.get(url, callback)
Ajax的GET方法

**Kind**: static method of [<code>hQuery</code>](#hQuery)  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>string</code> | 请求资源的地址 |
| callback | <code>function</code> | 回调函数 |

<a name="hQuery.post"></a>

### hQuery.post(url, data, callback)
Ajax的POST方法

**Kind**: static method of [<code>hQuery</code>](#hQuery)  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>string</code> | 请求资源的地址 |
| data | <code>form</code> | POST的数据 |
| callback | <code>function</code> | 回调函数 |

