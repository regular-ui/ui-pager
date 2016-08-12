## 示例
### 基本形式

<div class="m-example"></div>

```xml
<pager current=6 total=11 />
```

### 位置

<div class="m-example"></div>

```xml
<pager current=6 total=11 position="left" />
<pager current=6 total=11 position="center" />
<pager current=6 total=11 position="right" />
```

### 显示数目

<div class="m-example"></div>

```xml
<pager current=6 total=11 middle=3 side=1 />
```

### 禁用组件

<div class="m-example"></div>

```xml
<pager current=6 total=11 disabled />
```

### 数据绑定

<div class="m-example"></div>

```xml
<pager current={current} total=11 />
<p><span>当前页：{current}</span></p>
<a class="u-btn u-btn-info" on-click={current -= 1}>上一页</a>
<a class="u-btn u-btn-info" on-click={current += 1}>下一页</a>
```

```javascript
let component = new RGUI.Component({
    template,
    data: {current: 6},
});
```

### 事件

请打开浏览器的控制台查看结果。

<div class="m-example"></div>

```xml
<pager current=6 total=11
    on-select={console.log('on-select:', '$event.current:', $event.current)}
    on-change={console.log('on-change:', '$event.current:', $event.current)} />
```
