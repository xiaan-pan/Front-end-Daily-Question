# 隐藏元素的方法有哪些？有什么区别？

* display:none：渲染树不会包含该渲染对象，因此该元素不会在页面中占据位置，也不会响应绑定的监听事件。
* visibility:hidden：元素在页面中仍占据空间，但是不会响应绑定的监听事件。
* opacity:0：将元素的透明度设置为 0，以此来实现元素的隐藏。元素在页面中仍然占据空间，并且能够响应元素绑定的监听事件。
* position: absolute/fixed：通过使用绝对/固定定位将元素移除可视区域内，以此来实现元素的隐藏。
* z-index: 负值：来使其他元素遮盖住该元素，以此来实现隐藏。
* clip/clip-path ：使用元素裁剪的方法来实现元素的隐藏，这种方法下，元素仍在页面中占据位置，但是不会响应绑定的监听事件。
* transform:scale(0,0)：将元素缩放为 0，来实现元素的隐藏。这种方法下，元素仍在页面中占据位置，但是不会响应绑定的监听事件。

最常用的还是 display:none 和 visibility:hidden，其他的方式只能认为是奇招，它们的真正用途并不是用于隐藏元素，所以并不推荐使用它们。

关于 display:none、visibility:hidden、opacity:0 的区别，如下表所示：

display:none	visibility:hidden	opacity:0
页面中	不存在	存在	存在
重排	会	不会	不会
重绘	会	会	不一定
自身绑定事件	不触发	不触发	可触发
transition	不支持	支持	支持
子元素可复原	不能	能	不能
被遮挡的元素可触发事件	能	能	不能