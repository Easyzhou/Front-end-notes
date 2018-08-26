# href/src、link/import

#### URL、src、href
src 是指向物件的来源。href是指向需要连结的地方。url是通用的 "连结" 的专业代名词，在 HTML语法里几乎不会使用  
url不是属性，src和href是属性，src用于替换当前元素，href用于在当前文档和引用资源之间确立联系，也就是说src引用的路径是img自己的路径，href引用的路径是要跳转到的地方。 
#### link/import  
  差别1：老祖宗的差别。link属于XHTML标签，而@import完全是CSS提供的一种方式。
  link标签除了可以加载CSS外，还可以做很多其它的事情，比如定义RSS，定义rel连接属性等，@import就只能加载CSS了。  
  
  差别2：加载顺序的差别。当一个页面被加载的时候（就是被浏览者浏览的时候），link引用的CSS会同时被加载，而@import引用的CSS 会等到页面全部被下载完再被加载。所以有时候浏览@import加载CSS的页面时开始会没有样式（就是闪烁），网速慢的时候还挺明显（梦之都加载CSS 的方式就是使用@import，我一边下载一边浏览梦之都网页时，就会出现上述问题）  
  
  差别3：兼容性的差别。由于@import是CSS2.1提出的所以老的浏览器不支持，@import只有在IE5以上的才能识别，而link标签无此问题  
 
 差别4：使用dom控制样式时的差别。当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的  