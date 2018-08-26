# 边距重叠解决方案(BFC)
#### 边距重叠
边距重叠是指两个或多个盒子(可能相邻也可能嵌套)的相邻边界(其间没有任何非空内容、补白、边框)重合在一起而形成一个单一边界  
#### BFC
块级格式化上下文 (Block Fromatting Context)是按照块级盒子布局 
#### BFC的原理
    1、内部的box会在垂直方向，一个接一个的放置
    2、每个元素的margin box的左边，与包含块border box的左边相接触（对于从做往右的格式化，否则相反）
    3、box垂直方向的距离由margin决定，属于同一个bfc的两个相邻box的margin会发生重叠
    4、bfc的区域不会与浮动区域的box重叠
    5、bfc是一个页面上的独立的容器，外面的元素不会影响bfc里的元素，反过来，里面的也不会影响外面的
    6、计算bfc高度的时候，浮动元素也会参与计算
#### 怎么创建bfc（边距重叠产生原因）
    1、float属性不为none（脱离文档流）
    2、position为absolute或fixed，
    3、display为inline-block,table-cell,table-caption,flex,inine-flex
    4、overflow不为visible
    5、根元素的垂直margin不会被重叠
### 防止外边距重叠解决方案
    1、外层元素padding代替
    2、内层元素透明边框 border:1px solid transparent;
    3、内层元素绝对定位 postion:absolute:
    4、外层元素 overflow:hidden;
    5、内层元素 加float:left;或display:inline-block;
    6、内层元素padding:1px;
#### 应用场景
    1、自适应两栏布局
    2、清除内部浮动
    3、防止垂直margin重叠