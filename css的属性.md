css3的属性：

​	pointer-events: none; 可以用于指定某个特定的元素是否成为鼠标事件的target。



遮罩层的设置：首先，这个遮罩层需要一个差不多最外层的一个同级别的div，

```css
.div{
	position: absolute;
	top: 0;
	bottom: 0;
	left: 0;
	right: 0;
	background-color: rgba(0,0,0,0.8);
    z-index: 999;
}
// 这是需要引起注意的东西，通常在遮罩层上方
.highlight {
    position: absolute;
    z-index: 1000; //需要比div高
}
```

但这里会出来另一个问题。

我们需要在点击遮罩层再次取消，事件绑定到body上，但如果页面上有其他元素，这时候需要禁止触发。

给那些禁止触发click的元素绑定 

```css
pointer-events: none
```

属性。



还有种方法



