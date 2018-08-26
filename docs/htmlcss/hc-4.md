# 盒模型
盒模型的组成大家肯定都懂，由里向外content,padding,border,margin.  
盒模型是有两种标准的，一个是标准模型，一个是IE模型。  
#### 标准模型
在标准模型中，盒模型的宽高只是内容（content）的宽高  
#### IE模型
盒模型的宽高是内容(content)+填充(padding)+边框(border)的总宽高  
#### css如何设置两种模型
    1、标准模型 box-sizing:content-box;
    2、IE模型 box-sizing:border-box;
#### JS获取宽高如何获取盒模型对应的宽高
    1、dom.style.width/height  
	这种方式只能取到dom元素内联样式所设置的宽高，也就是说如果该节点的样式是在style标签中或外联的CSS文件中
	设置的话，通过这种方法是获取不到dom的宽高的  
    2、dom.currentStyle.width/height  
    这种方式获取的是在页面渲染完成后的结果，就是说不管是哪种方式设置的样式，都能获取到，只有IE浏览器支持该方式  
    3、window.getComputedStyle(dom).width/height   
	这种方式的原理和2是一样的，这个可以兼容更多的浏览器，通用性好一些  
	4、 dom.getBoundingClientRect().width/height  
	这种方式是根据元素在视窗中的绝对位置来获取宽高的  
	5、 dom.offsetWidth/offsetHeight  
