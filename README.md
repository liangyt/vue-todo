# vue

如果要把一个输入框输入的内容展示在不同的地方，你会怎么怎么实现呢？

```
<input id="id" />

<div id="to"></div>
```



> * 写原生的同学
```
var source = document.getElementById('#id').value;
var to =  document.gtElementById('#to');
to.innerText = source;
```
>* 写jQuery的同学
```
var source = $('#id').val();
var to = $('#to');
to.text(source);
```

>*  写Vue的同学

```
<div id="app">
	<input v-model="msg" />
	<div>{{msg}}</div>
</div>

new Vue({
	el:'#app',
    data:{
    	msg:''
    }
})
```

看过之后是不是发现也没有简单多少呢？ 

### 正式介绍一下Vue
概述：Vue.js（读音 /vjuː/, 类似于 view）是一个构建数据驱动的 web 界面的库。Vue.js 的目标是通过尽可能简单的 API 实现响应的数据绑定和组合的视图组件。

Vue.js 自身不是一个全能框架——它只聚焦于视图层。因此它非常容易学习，非常容易与其它库或已有项目整合。另一方面，在与相关工具和支持库一起使用时，Vue.js 也能完美地驱动复杂的单页应用。

Vue.js 的核心是一个响应的数据绑定系统，它让数据与 DOM 保持同步非常简单。


下面一起看看咱们经常使用的Vue的基本用法/语法：

>* 实例化
```
var vm = new Vue({
  // 选项
})
```

>* 常用配置项
