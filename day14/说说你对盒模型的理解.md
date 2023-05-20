# 说说你对盒模型的理解

盒模型都是由四个部分组成的，分别是 margin、border、padding 和 content。
CSS 中的盒模型有以下两种：标准盒子模型、IE盒子模型

标准盒模型和IE盒模型的区别在于设置 width 和 height 时，所对应的范围不同：

* 标准盒模型的width和height属性的范围只包含了content
  
* IE盒模型的width和height属性的范围包含了 border、padding 和 content。

可以通过修改元素的 box-sizing 属性来改变元素的盒模型：

* box-sizeing: content-box 表示标准盒模型（默认值）
* box-sizeing: border-box 表示IE盒模型（怪异盒模型）