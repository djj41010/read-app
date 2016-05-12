##### 单例与实例化
单例实际就是一个obj，好处是不用每次实例化。节省内存。
```javascript
var single = {
	attr_1: '1',
	func: function(){
	console.log(1)
},
}
//使用
single.attr_1//'1'
single.func()//1
```
实例化不同于单例，根据此对象或者类来实例化多个对象，ES6新加了class用法，以前使用function来声明构造函数--java中的类。
```javascript
function class_A(param){
	this.attr_1 = param;
	this.func_1 = function(){
	console.log(this.attr_1);
};
}
var instance_1 = new class_A('1');
var instance_2 = new class_A('2');
```
base64图片制作icon，可减少请求
`background:url(data:image/png;base64,{img_data}`；
移动端的两个性能方面的影响：repaint重绘，reflow回流(减少dom元素的操作)；能缓存的尽量缓存。
localStorage.setItem():只能缓存字符串，若想存对象的话localStorage.setItem('data',JSON.stringify({}));JSON.parse(localStorage.getItem('data',JSON.stringify({})))
非static元素尽量不适用css动画。
overflow-x:hidden;