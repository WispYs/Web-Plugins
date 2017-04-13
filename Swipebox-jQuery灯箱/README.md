jQuery灯箱效果插件-Swipebox
================================

[官方地址](http://brutaldesign.github.com/swipebox)

Swipebox 是一款可触摸的 jQuery 灯箱效果插件，可用于桌面，移动和平板电脑。 支持移动设备滑动手势导航，桌面电脑上可以用键盘导航，不支持 CSS3 过渡特性的浏览器使用 jQuery 降级处理，支持视网膜显示，能够通过 CSS 轻松定制。

## 主要特点

- 滑动手势移动
- 键盘导航的桌面
- CSS过渡使用jQuery后备
- 针对UI图标支持视网膜
- 简单的CSS定制


### 兼容

Chrome, Safari, Firefox, Opera, IE9+, IOS4+, Android, windows phone.

## 基本用法

### Javascript

在您的页面中添加jQuery和swipebox脚本

	<script src="lib/jquery-1.9.0.js"></script>
	<script src="src/js/jquery.swipebox.js"></script>


### CSS

在您的页面中添加swipebox CSS样式标签。

```html
<link rel="stylesheet" href="src/css/swipebox.css">
```

### HTML

使用特定的类为你的链接和使用title属性为标题。

```html
<a href="big/image.jpg" class="swipebox" title="My Caption">
```

### 绑定了“swipebox”类。

```javascript
$( '.swipebox' ).swipebox();
```
### 视频支持

只需在您的href属性粘贴视频网址。该脚本会自动检查它是否是一个视频网址，并在打开的swipebox视频。

	<a class="swipebox-video" rel="视频" href="#">My Videos</a>
	
### 动态加载的幻灯片

你可以通过一个数组对象传递给swipebox动态设置您的画廊。

	$("#gallery").click(function(e){
		e.preventDefault();
		$.swipebox([
			{href:'big/image1.jpg', title:'My Caption'}, 
			{href:'big/image2.jpg', title:'My Second Caption'}
		]);
	});
### 刷新方法

刷新方法可以让你重新加载幻灯片，如果在DOM发生了变化。

	var swipeboxInstance = $(".a:visible").swipebox();
	// Use the refresh method after your event is completed
	swipeboxInstance.refresh();
### 检查打开状态

	if ($.swipebox.isOpen){
		// do stuff
	}
### 选项

```javascript
useCSS : true, // false will force the use of jQuery for animations
initialIndexOnArray: 0, // which image index to init when a array is passed
removeBarsOnMobile : true, // false will show top navigation bar on mobile devices
hideCloseButtonOnMobile : false, // true will hide the close button on mobile devices
removeBarsOnMobile : true, // false will show bottom bar on mobile devices
hideBarsDelay : 3000, // delay before hiding bars on desktop
videoMaxWidth : 1140, // videos max width
beforeOpen: function(){} , // called before opening
afterOpen: null, // called after opening
afterClose: function(){}, // called after closing
afterMedia: function(){}, // called after media is loaded
loopAtEnd: false, // true will return to the first image after the last image is reached
autoplayVideos: false // true will autoplay Youtube and Vimeo videos
queryStringData: {} // plain object with custom query string arguments to pass/override for video URLs,
toggleClassOnLoad: '' // CSS class that can be toggled when the slide will be loaded (like 'hidden' of Bootstrap)
useSVG: true
```

