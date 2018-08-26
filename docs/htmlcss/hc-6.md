# 浮动float

#### 误解和误用
 float 被设计出来的初衷是用于文字环绕效果，即一个图片一段文字，图片float:left之后，文字会环绕图片  
 但是，后来大家发现结合float + div可以实现之前通过table实现的网页布局，因此就被“误用”于网页布局了
 
#### 为何 float 会导致父元素塌陷？
float 的破坏性 —— float 破坏了父标签的原本结构，使得父标签出现了坍塌现象。导致这一现象的最根本原因在于：被设置了 float 的元素会脱离文档流，我们的浮动是左右浮动，所以我们的块级元素都是左右排列。其根本原因在于 float 的设计初衷是解决文字环绕图片的问题  

包裹性也是 float 的一个非常重要的特性，普通的 div 如果没有设置宽度，它会撑满整个屏幕，在之前的盒子模型那一节也讲到过。而如果给 div 增加float:left之后，它突然变得紧凑了，宽度发生了变化，把内容中的三个字包裹了——这就是包裹性。为 div 设置了 float 之后，其宽度会自动调整为包裹住内容宽度，而不是撑满整个父容器  

清空格，对于高度不同的容器，float 排版出来的网页严丝合缝，

#### 清除浮动（clear）

    1、额外添加标签，再最后一个浮动的盒子的后面，新添加一个标签。然后他可以清除浮动  
    2、Overflow 清除浮动，是浮动的大盒子（父级标签）再样式里面加: overflow:hidden，  
	常用的ul li，在ul里添加overflow：hidden  
	3、After伪类清除浮动  
	4、写一个通用的clearfix类，直接在需要清除浮动的地方加一个这个样式 ：<div class="box clearfix">
	5、After before伪类清除浮动 是大部分大型网站常用的，比如新浪 淘宝 的清除浮动的效果  
	.clearfix:before,.clearfix:after{  
		content:"";  
		display:table;  
		}  
		.clearfix:after{  
		clear:both;  
		}  
		.clearfix{ /*照顾ie6*/  
		zoom:1;  
		}  
		使用：  
		<div class="box clearfix">  
