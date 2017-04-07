Tippy.js-纯js tooltip工具提示插件
----
Tippy.js是一款轻量级的纯js tooltip工具提示插件。该tooltip插件功能强大，提供多种动画效果和主题效果，并允许用户自定义tooltip主题和使用html代码作为tooltip的模板。

[官方地址](http://www.htmleaf.com/jQuery/Tooltips/201704054439.html)
  
 ## 预览
 ![Tippy](https://github.com/WispYs/Web-Plugins/blob/master/img/tippy.png "Tippy")

 ## 安装
 可以通过npm来安装在Tippy.js插件。
				npm install --save tippy.js    

 ## 使用方法
 在页面中引入tippy.js和tippy.css文件。
				<link rel="stylesheet" href="css/tippy.css">
				<script src='path/to/tippy.js'></script>  
				
 ## HTML结构
 你需要为使用tooltip的元素设置一个title属性，这个属性中的内容就是tooltip的内容。
				<button class="btn tippy" title="I'm a tooltip!">tooltip测试</button> 

 ## 初始化插件
 在页面DOM元素加载完毕之后，通过new Tippy()方法来实例化tooltip。
				new Tippy('.tippy') 
 一个完整的使用tippy.js的HTML文档的结构如下：
				<!DOCTYPE html>
				<html>
				  <head>
					<link rel="stylesheet" href="tippy.css">
				  </head>
				  <body>
					<button id="myId" title="Tooltip text">Button text</button>
					<script src="tippy.js"></script>
					<script>
					new Tippy('#myId')
					</script>
				  </body>
				</html>
 ## 配置参数
 详细参数请看[官方文档](http://www.htmleaf.com/jQuery/Tooltips/201704054439.html)