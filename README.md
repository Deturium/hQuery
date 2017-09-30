# hQuery


## 自己实现的jQuery

- 参考jQuery的API设计

- 支持链式调用

- 只兼容高版本浏览器

- 未经的测试


# 文档

## Classes

<dl>
<dt><a href="#H">H</a></dt>
<dd></dd>
</dl>

## Members

<dl>
<dt><a href="#hQuery">hQuery</a></dt>
<dd></dd>
</dl>

<a name="H"></a>

## H
**Kind**: global class  

* [H](#H)
    * [new H(selector, [context])](#new_H_new)
    * _instance_
        * [.find(selector)](#H+find) ⇒ [<code>H</code>](#H)
        * [.first()](#H+first) ⇒ [<code>H</code>](#H)
        * [.last()](#H+last) ⇒ [<code>H</code>](#H)
        * [.eq(num)](#H+eq) ⇒ [<code>H</code>](#H)
        * [.parent()](#H+parent) ⇒ [<code>H</code>](#H)
        * [.children()](#H+children) ⇒ [<code>H</code>](#H)
        * [.next()](#H+next) ⇒ [<code>H</code>](#H)
        * [.prev()](#H+prev) ⇒ [<code>H</code>](#H)
        * [.slice(start, end)](#H+slice) ⇒ [<code>H</code>](#H)
        * [.filter(fn)](#H+filter) ⇒ [<code>H</code>](#H)
        * [.end()](#H+end) ⇒ [<code>H</code>](#H)
        * [.html([html])](#H+html) ⇒ <code>string</code> \| [<code>H</code>](#H)
        * [.text([text])](#H+text) ⇒ <code>string</code> \| [<code>H</code>](#H)
        * [.val([value])](#H+val) ⇒ <code>string</code> \| [<code>H</code>](#H)
        * [.attr(attr, [value])](#H+attr) ⇒ <code>string</code> \| [<code>H</code>](#H)
        * [.append(html)](#H+append) ⇒ [<code>H</code>](#H)
        * [.prepend(html)](#H+prepend) ⇒ [<code>H</code>](#H)
        * [.remove()](#H+remove) ⇒ [<code>H</code>](#H)
        * [.replaceWith(html)](#H+replaceWith) ⇒ [<code>H</code>](#H)
        * [.hide()](#H+hide) ⇒ [<code>H</code>](#H)
        * [.show()](#H+show) ⇒ [<code>H</code>](#H)
        * [.toggle()](#H+toggle) ⇒ [<code>H</code>](#H)
        * [.css(attr, [value])](#H+css) ⇒ <code>string</code> \| [<code>H</code>](#H)
        * [.hasClass(className)](#H+hasClass) ⇒ <code>boolean</code>
        * [.addClass(className)](#H+addClass) ⇒ [<code>H</code>](#H)
        * [.removeClass(className)](#H+removeClass) ⇒ [<code>H</code>](#H)
        * [.toggleClass(className, [force])](#H+toggleClass) ⇒ [<code>H</code>](#H)
        * [.on(event, handler)](#H+on) ⇒ [<code>H</code>](#H)
        * [.off(event, handler)](#H+off) ⇒ [<code>H</code>](#H)
        * [.one(event, handler)](#H+one) ⇒ [<code>H</code>](#H)
        * [.each(fn)](#H+each) ⇒ [<code>H</code>](#H)
    * _static_
        * [.extend(name, fn)](#H.extend) ⇒ [<code>H</code>](#H)

<a name="new_H_new"></a>

### new H(selector, [context])
hQuery构造函数，可以直接h()调用

**Returns**: [<code>H</code>](#H) - - 返回hQuery对象  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| selector | <code>String</code> \| <code>DOM</code> |  | 将querySelectAll的选择器 |
| [context] | <code>DOM</code> | <code>document</code> | 作为选择器的起点 |

<a name="H+find"></a>

### h.find(selector) ⇒ [<code>H</code>](#H)
以当前对象的第一个节点为根节点，返回符合选择器的子节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuey对象  

| Param | Type | Description |
| --- | --- | --- |
| selector | <code>string</code> | 选择器 |

<a name="H+first"></a>

### h.first() ⇒ [<code>H</code>](#H)
返回被选中的第一个节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuey对象  
<a name="H+last"></a>

### h.last() ⇒ [<code>H</code>](#H)
返回被选中的最后一个节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
<a name="H+eq"></a>

### h.eq(num) ⇒ [<code>H</code>](#H)
返回被选中的第n个节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| num | <code>number</code> | 从0开始指定第num个节点，可接受负数 |

<a name="H+parent"></a>

### h.parent() ⇒ [<code>H</code>](#H)
返回第一个节点的父节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
<a name="H+children"></a>

### h.children() ⇒ [<code>H</code>](#H)
返回第一个节点的所有子节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
<a name="H+next"></a>

### h.next() ⇒ [<code>H</code>](#H)
返回所有节点的下一个兄弟节点集合，忽略文本节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
<a name="H+prev"></a>

### h.prev() ⇒ [<code>H</code>](#H)
返回所有节点的前一个兄弟节点集合，忽略文本节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
<a name="H+slice"></a>

### h.slice(start, end) ⇒ [<code>H</code>](#H)
返回[start, end)的节点集合

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| start | <code>number</code> | 起点 |
| end | <code>number</code> | 终点 |

<a name="H+filter"></a>

### h.filter(fn) ⇒ [<code>H</code>](#H)
返回满足筛选函数的节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  

| Param | Type | Description |
| --- | --- | --- |
| fn | <code>function</code> | 用作筛选的函数，应返回boolean值 |

<a name="H+end"></a>

### h.end() ⇒ [<code>H</code>](#H)
回溯到链上的上一个hQuery对象

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 全新的hQuery对象  
**Example**  
```js
h('#id').find('.class').end() // 会被回溯到h('#id')
```
<a name="H+html"></a>

### h.html([html]) ⇒ <code>string</code> \| [<code>H</code>](#H)
返回或者设置节点的html

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: <code>string</code> \| [<code>H</code>](#H) - 返回html内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [html] | <code>string</code> | 将要设置的html值 |

<a name="H+text"></a>

### h.text([text]) ⇒ <code>string</code> \| [<code>H</code>](#H)
返回或者设置节点的text

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: <code>string</code> \| [<code>H</code>](#H) - 返回text内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [text] | <code>string</code> | 将要设置的text值 |

<a name="H+val"></a>

### h.val([value]) ⇒ <code>string</code> \| [<code>H</code>](#H)
返回或者设置节点的value

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: <code>string</code> \| [<code>H</code>](#H) - 返回value内容或者自身  

| Param | Type | Description |
| --- | --- | --- |
| [value] | <code>string</code> | 将要设置的value值 |

<a name="H+attr"></a>

### h.attr(attr, [value]) ⇒ <code>string</code> \| [<code>H</code>](#H)
返回或者设置节点的属性

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: <code>string</code> \| [<code>H</code>](#H) - 返回属性值或者自身  

| Param | Type | Description |
| --- | --- | --- |
| attr | <code>string</code> \| <code>object</code> | 想取得或者将要设置的attr值，可直接传入{ attr: value }的对象 |
| [value] | <code>string</code> | 要设置的attr值 |

<a name="H+append"></a>

### h.append(html) ⇒ [<code>H</code>](#H)
在节点的子节点末尾添加html

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 想要添加的html或者节点，DOM可以传入多个 |

<a name="H+prepend"></a>

### h.prepend(html) ⇒ [<code>H</code>](#H)
在节点的子节点开头添加html

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 想要添加的html或者节点，DOM可以传入多个 |

<a name="H+remove"></a>

### h.remove() ⇒ [<code>H</code>](#H)
删除节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  
<a name="H+replaceWith"></a>

### h.replaceWith(html) ⇒ [<code>H</code>](#H)
替代当前节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| html | <code>string</code> \| <code>DOM</code> | 用以替换的html或者节点，DOM可以传入多个 |

<a name="H+hide"></a>

### h.hide() ⇒ [<code>H</code>](#H)
隐藏节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  
<a name="H+show"></a>

### h.show() ⇒ [<code>H</code>](#H)
显示节点

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  
<a name="H+toggle"></a>

### h.toggle() ⇒ [<code>H</code>](#H)
切换隐藏和显示的状态

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - - 返回自身  
<a name="H+css"></a>

### h.css(attr, [value]) ⇒ <code>string</code> \| [<code>H</code>](#H)
返回或者设置节点的css

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: <code>string</code> \| [<code>H</code>](#H) - 返回属性值或者自身  

| Param | Type | Description |
| --- | --- | --- |
| attr | <code>string</code> \| <code>object</code> | 想取得或者将要设置的css值，可直接传入{ attr: value }的对象 |
| [value] | <code>string</code> | 要设置的css值 |

<a name="H+hasClass"></a>

### h.hasClass(className) ⇒ <code>boolean</code>
检测节点是否有该class

**Kind**: instance method of [<code>H</code>](#H)  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 检测的类名 |

<a name="H+addClass"></a>

### h.addClass(className) ⇒ [<code>H</code>](#H)
为节点添加class

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 想增加的类名 |

<a name="H+removeClass"></a>

### h.removeClass(className) ⇒ [<code>H</code>](#H)
为节点去除class

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 想去除的类名 |

<a name="H+toggleClass"></a>

### h.toggleClass(className, [force]) ⇒ [<code>H</code>](#H)
切换class

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | 想切换的类名 |
| [force] | <code>boolen</code> | 可选切换方式，true表示增加，false表示去除 |

<a name="H+on"></a>

### h.on(event, handler) ⇒ [<code>H</code>](#H)
增加绑定事件

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数，记得处理this绑定 |

<a name="H+off"></a>

### h.off(event, handler) ⇒ [<code>H</code>](#H)
去除绑定事件

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数 |

<a name="H+one"></a>

### h.one(event, handler) ⇒ [<code>H</code>](#H)
增加绑定事件，该事件在触发一次后会被移除

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| event | <code>string</code> | 事件名 |
| handler | <code>function</code> | 回调函数，记得处理this绑定 |

<a name="H+each"></a>

### h.each(fn) ⇒ [<code>H</code>](#H)
对每一个节点调用处理函数

**Kind**: instance method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| fn | <code>function</code> | 处理函数，如果返回false会中断后续执行 |

<a name="H.extend"></a>

### H.extend(name, fn) ⇒ [<code>H</code>](#H)
在hQuery的原型链上扩展新的方法

**Kind**: static method of [<code>H</code>](#H)  
**Returns**: [<code>H</code>](#H) - 返回自身  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>name</code> | 新增的方法名 |
| fn | <code>function</code> | 新增的方法 |

<a name="hQuery"></a>

## whQuery
hQuery暴露在外的接口

**Kind**: global variable  