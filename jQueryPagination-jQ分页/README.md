jQueryPagination-jQ分页
----

插件描述：jQuery分页插件

根据获取内容显示不同页数并可输入页码跳转

[官方地址](http://www.jq22.com/jquery-info3813)
  
 ## 预览
 ![Page](https://github.com/WispYs/Web-Plugins/blob/master/img/page.png "Page")
 
 ### 标注
 回调函数
	$("#Pagination").pagination("15",{
		load_first_page:true,//插件加载时是否回调当前页码
		callback:function(current_page){
			//回调函数,当前页码为current_page，页码编号从0开始
			console.log(current_page)
		}
	});
