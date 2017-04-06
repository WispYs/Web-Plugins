### Simditor 是团队协作工具 Tower 使用的富文本编辑器。

相比传统的编辑器它的特点是：


    * 功能精简，加载快速
    * 输出格式化的标准 HTML
    * 每一个功能都有非常优秀的使用体验
    * 兼容的浏览器：IE10+、Chrome、Firefox、Safari。



第一步：下载并引用

在这里下载并解压最新版的 Simditor 文件，然后在页面中引入这些文件：


<link rel="stylesheet" type="text/css" href="[style path]/font-awesome.css" />
<link rel="stylesheet" type="text/css" href="[style path]/simditor.css" />
<script type="text/javascript" src="[script path]/jquery.min.js"></script>
<script type="text/javascript" src="[script path]/module.js">
</script><script type="text/javascript" src="[script path]/uploader.js">
</script><script type="text/javascript" src="[script path]/simditor.js"></script>
其中，

Simditor基于 jQuery 开发，jquery.js 是必需的；

font-awesome.css 是一个图片字体 icon 库，Simditor 基于它来定义工具栏的按钮样式。为了让 icon 能够正常显示，需要将 font 文件（fontawesome-webfont.xxx）放到正确的路径里：../fonts/（如果把 font-awsome.css 放在 styles 文件夹，那么就应该把 font 文件放在跟 styles 同级的 fonts 文件夹）。另外，如果想自定义工具栏按钮的样式就可以不必引用 font-awesome.css；

module.js 是彩程内部使用的 CoffeeScript 组件抽象类，Simditor 基于这个类开发；

uploader.js 是一个与 UI 无关的上传逻辑，如果你的项目不需要上传附件，那么可以不引用这个文件。

如果觉得需要引用的脚本文件太多，可以用 simditor-all.js（里面包含了module.js uploader.js 和 simditor.js）替换：

<link rel="stylesheet" type="text/css" href="[style path]/font-awesome.css" /> 
<link rel="stylesheet" type="text/css" href="[style path]/simditor.css" /> 
<script type="text/javascript" src="[script path]/jquery-2.1.0.js">
</script> <script type="text/javascript" src="[script path]/simditor-all.js"></script>


第二步，初始化配置

在使用 Simditor 的 HTML 页面里应该有一个对应的 textarea 文本框，例如：

<textarea id="editor" placeholder="这里输入内容" autofocus></textarea>
我们需要在这个页面的脚本里初始化 Simditor：

var editor = new Simditor({   textarea: $('#editor') });

textarea 是初始化 Simditor 的必需选项，可以接受 jQuery Object、HTML Element 或者 Selector String。另外，Simditor 还支持这些可选 option：

placeholder（默认值：''）编辑器的 placeholder，如果为空 Simditor 会取 textarea 的 placeholder 属性；

toolbar （默认值：true）是否显示工具栏按钮；

toolbarFloat （默认值：true）是否让工具栏按钮在页面滚动的过程中始终可见；

toolbarHidden （默认值：false）是否隐藏工具栏，隐藏后 toolbarFloat 会失效；

defaultImage（默认值：'images/image.png'）编辑器插入混排图片时使用的默认图片；

tabIndent（默认值：true）是否在编辑器中使用 tab 键来缩进；

params（默认值：{}）键值对，在编辑器中增加 hidden 字段（input:hidden），通常用于生成 form 表单的默认参数；

upload（默认值：false）false 或者键值对，编辑器上传本地图片的配置，常用的属性有 url 和 params；

pasteImage（默认值：false）是否允许粘贴上传图片，依赖 upload 选项，仅支持 Firefox 和 Chrome 浏览器。

更详细的配置说明可以参考 Simditor 的配置文档。配置完成之后刷新页面，Simditor 应该就可以正确加载了。



最后，自定义样式和交互

每个项目都有不同的设计风格，大多数时候我们需要修改 Simditor 的样式，让它的样式跟项目的风格相符。

simditor.css 是通过 Sass 自动生成的代码，所以推荐大家修改 simditor.scss，然后再重新生成css代码。

.editor-style 选择符下面的样式，是 Simditor 输出 HTML 的中文排版样式，大家可以根据自己项目的情况进行调整。另外，如果不想使用 font-awesome.css 来实现工具栏按钮的 icon，可以将 font-awesome.css 去掉，然后增加 .toolbar-item-[button name] 选择符来自定义按钮样式。
