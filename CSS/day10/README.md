# 谈谈你对 BFC 的理解

块格式化上下文（Block Formatting Context，BFC）是 Web 页面的可视化 CSS 渲染的一部分，是布局过程中生成块级盒子的区域，也是浮动元素与其他元素的交互限定区域。

通俗来讲：BFC 是一个独立的布局环境，可以理解为一个容器，在这个容器中按照一定规则进行物品摆放，并且不会影响其它环境中的物品。如果一个元素符合触发BFC的条件，则BFC中的元素布局不受外部影响。 

BFC的特点：
* 垂直方向上，自上而下排列，和文档流的排列方式一致。
* 在 BFC 中上下相邻的两个容器的 margin 会重叠
* 计算 BFC 的高度时，需要计算浮动元素的高度
* BFC 区域不会与浮动的容器发生重叠
* BFC 是独立的容器，容器内部元素不会影响外部元素
* 每个元素的左 margin 值和容器的左 border 相接触

创建BFC
1. html 根元素
2. 浮动元素（float 值不为 none）
3. 绝对或固定定位元素（position 值为 absolute 或 fixed
4. display＝inline-block|flex|inline-flex|table-cell或table-caption
5. overflow 值不为 visible

BFC 的应用：
* 解决 margin 的重叠问题：由于 BFC 是一个独立的区域，内部的元素和外部的元素互不影响，将两个元素变为两个 BFC，就解决了 margin 重叠的问题。
* 解决高度塌陷的问题：在对子元素设置浮动后，父元素会发生高度塌陷，也就是父元素的高度变为0。解决这个问题，只需要把父元素变成一个 BFC。常用的办法是给父元素设置 overflow:hidden。
* 创建自适应两栏布局：可以用来创建自适应两栏布局：左边的宽度固定，右边的宽度自适应。