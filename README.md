# PictureSlider
使用jQuery编写的图片幻灯片轮播插件

###兼容性
IE7.0及其以上的IE版本；Firefox30；Chrome27

###使用方法
html部分代码
```HTML
<div class="pictureSlider poster-main" data-setting='{}'>
	<!-- 前一张按钮-->
	<div class="poster-btn poster-prev-btn"></div>
    <ul class="poster-list">
    	<!-- 图片路径 -->
    	<li class="poster-item"><a href="#"><img src="1.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="2.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="3.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="4.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="5.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="2.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="3.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="4.jpg" width="100%" height="100%"></a></li>
        <li class="poster-item"><a href="#"><img src="5.jpg" width="100%" height="100%"></a></li>
    </ul>
    <!-- 下一张按钮-->
    <div class="poster-btn poster-next-btn"></div>
</div>
```
其中data-setting用于设置用户自定义参数，主要的设置参数有：  
总的宽度width  
总的高度height  
当前展示图片的宽度posterWidth  
当前展示图片的高度posterHeight  
图片之间的缩放比例scale  
是否启动自动播放autoplay  
图片之间的切换时间delay  
图片切换速度speed  
设置图片的对齐方式vertecalAlign，有三种对其方式，分别是：top, middle, bottom  
如果没有设置，则所有的参数采用默认值；如需要设置，则使用JSON格式，如：  
data-setting{  
	"width":1000,  
	"height":270,  
	"posterWidth":640,  
	"posterHeight":270,  
	"scale":0.8,  
	"autoPlay":true,  
	"delay":2000,  
	"speed":300,  
	"verticalAlign":"middle"  
}  

JavaScript部分代码  
1) 首先引用jQuery文件  
2) 调用插件的初始化函数  
```Javascript
$(function(){
	Carousel.init($(".pictureSlider"));
});
```
