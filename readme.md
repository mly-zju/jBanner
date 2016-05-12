##jBanner
一款轻量但是强大的焦点图组件，可以实现多种焦点图轮播效果。组件持续开发中，未来还将实现更多酷炫的效果哦！
* 在线演示: http://mly-zju.github.io/project/jBanner/demo.html

##依赖关系与版本
* 组件是基于jquery的，所以在使用之前，请首先导入jquery库。
* 支持浏览器版本号：Internet Explorer 10+, Chrome, Firefox, Safari

##使用方法
首先，在html文件头引入jbanner.js（路径名不同项目不一样，自行确定）:
```html
<script type='text/javascript' src='jbanner.js'></script>
```
其次，在需要使用焦点图的地方插入一个div标签作为容器，并在class中加入名称jBanner-wrapper:
```html
<div class='jBanner-wrapper'></div>
```
该div的height和width根据应用需要自行确定。
最后，在script脚本中加入如下语句：
```jquery
$('.jBanner-wrapper').jBannerInit(options);
```
其中options是一个对象，有如下成员：

* imgURL:是一个数组，包含有焦点图图片的路径，都是以字符串的形式存放，如：['./img/0.jpg','./img/1.jpg']
* imgWidth:焦点图图片的宽度，数字。该图片宽度应该等同于容器（即.jBanner-wrapper）的宽度。
* imgHeight:焦点图图片的高度，数字。同样应该等同于容器的高度。
* mode:焦点图切换效果选项，字符串。可选项有：
  *  "fade":淡入淡出效果
  *  "slide":滑入滑出效果
  *  "box":盒状切换效果
  *  "blind":百叶窗切换效果
  *  "vertical-blind":垂直百叶窗切换效果
  *  "stripe":条纹切换效果
  *  "vertical-stripe":垂直条纹切换效果
  mode默认选项为fade模式。
* autoPlay:焦点图图片是否自动切换，布尔型。默认为true，即自动切换
* interval:焦点图图片切换时间间隔(毫秒)，默认为3000 ms，且最小间隔为1500 ms(小于1500将自动设置为1500)。当autoPlay为false，设置此参数无效

一个options的例子：
```javascript
var options={
    imgURL:['./img/0.jpg','./img/1.jpg','./img/2.jpg'],
    imgWidth:800,
    imgHeight:400,
    mode:'vertical-stripe'
};
```

##关于作者
* 个人网站: http://mly-zju.github.io
