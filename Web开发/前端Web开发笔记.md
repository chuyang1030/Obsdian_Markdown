# 前端Web开发
一个网页由以下部分组成：
- HTML：负责网页的结构（页面元素和内容）。
    
- CSS：负责网页的表现（页面元素的外观、位置等页面样式，如：颜色、大小等）。
    
- JavaScript：负责网页的行为（交互效果例如点击 警告......）。
- Js高级框架Vue

### JSON自定义对象
var 对象名 = {
    属性名1: 属性值1, 
    属性名2: 属性值2,
    属性名3: 属性值3,
    函数名称: function(形参列表){}
};
```js
var jsonstr = '{"name":"Tom", "age":18, "addr":["北京","上海","西安"]}';
alert(jsonstr.name);//undefinded
```
```js
var obj = JSON.parse(jsonstr);
alert(obj.name);//Tom、
```当然了，我们也可以通过如下函数将json对象再次转换成json字符串。添加如下代码：
```js
alert(JSON.stringify(obj));
```

### BOM对象

BOM的全称是Browser Object Model,翻译过来是浏览器对象模型。也就是JavaScript将浏览器的各个组成部分封装成了对象。我们要操作浏览器的部分功能，可以通过操作BOM对象的相关属性或者函数来完成。例如：我们想要将浏览器的地址改为`http://www.baidu.com`,我们就可以通过BOM中提供的location对象的href属性来完成，代码如下：`location.href='http://www.baidu.com'`

BOM中提供了如下5个对象：

| 对象名称      | 描述      |
| --------- | ------- |
| Window    | 浏览器窗口对象 |
| Navigator | 浏览器对象   |
| Screen    | 屏幕对象    |
| History   | 历史记录对象  |
| Location  | d地址栏对象  |

### DOM对象
对象分为

- Document：整个文档对象
- Element：元素对象
- Attribute：属性对象
- Text：文本对象
- Comment：注释对象

作用：
- 改变 HTML 元素的内容
- 改变 HTML 元素的样式（CSS）
- 对 HTML DOM 事件作出反应
- 添加和删除 HTML 元素

获取DOM对象：

| 函数                                | 描述                         |
| --------------------------------- | -------------------------- |
| document.getElementById()         | 根据id属性值获取，返回单个Element对象    |
| document.getElementsByTagName()   | 根据标签名称获取，返回Element对象数组     |
| document.getElementsByName()      | 根据name属性值获取，返回Element对象数组  |
| document.getElementsByClassName() | 根据class属性值获取，返回Element对象数组 |
代码示例：
```html
<script>
//1. 获取Element元素

//1.1 获取元素-根据ID获取
 var img = document.getElementById('h1');
 alert(img);
</script>
```

## Vue

- Model: 数据模型，特指前端中通过请求从后台获取的数据
- View: 视图，用于展示数据的页面，可以理解成我们的html+css搭建的页面，但是没有数据
- ViewModel: 数据绑定到视图，负责将数据（Model）通过JavaScript的DOM技术，将数据展示到视图（View）上

其中的Model我们可以通过Ajax来发起请求从后台获取;对于View部分，我们将来会学习一款ElementUI框架来替代HTML+CSS来更加方便的搭建View;而今天我们要学习的就是侧重于ViewModel部分开发的vue前端框架，用来替代JavaScript的DOM操作，让数据展示到视图的代码开发变得更加的简单。

在js代码区域定义vue对象,代码如下：

```html
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
            message: "Hello Vue"
        }
    })
</script>
```

在创建vue对象时，有几个常用的属性：

- el: 用来指定哪儿些标签受 Vue 管理。 该属性取值 `#app` 中的 `app` 需要是受管理的标签的id属性值
- data: 用来定义数据模型
- methods: 用来定义函数。这个我们在后面就会用到

### Ajax概述

我们前端页面中的数据，如下图所示的表格中的学生信息，应该来自于后台，那么我们的后台和前端是互不影响的2个程序，那么我们前端应该如何从后台获取数据呢？因为是2个程序，所以必须涉及到2个程序的交互，所以这就需要用到我们接下来学习的Ajax技术。
### Ajax技术的2个作用
1.与服务器进行数据交互
2.异步交互：可以在**不重新加载整个页面**的情况下，与服务器交换数据并**更新部分网页**的技术。
### Axios
上述原生的Ajax请求的代码编写起来还是比较繁琐的，所以接下来我们学习一门更加简单的发送Ajax请求的技术Axios 。Axios是对原生的AJAX进行封装，简化书写。

## Element组件的使用

## Nginx对前端项目的打包部署
