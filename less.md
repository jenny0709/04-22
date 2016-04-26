# less
less是一门css预处理语言

跟它一样的有 Sass $  less @
> less可以让我们像编程一样，编写css。

## 使用less
  1.客户端用
  	//1>.写的要生成  css的less代码
  	<link rel="stylesheet/less" type="text/css" href="styles.less">

  	//2>.less.js库作用就是 编译less为css代码
  	<script type="text/javascript" src="less.js"></script>
  	less.js只能放在最后边

  2.服务端用
  把less 生成为 css文件
  1>.node.js
  	javascript 运行在浏览器、运行在客户端
  	node.js是javasript的一个服务器端运行环境
  	node.js语法是基于ECMAscript
  	php jsp asp 一样，可以作为后台语言
	
	npm 包管理工具 CLI(命令行)

	npm install 模块名  eg:npm install jquery

	npm install http:server 提供http服务的一个包
	npm包装的方式有两种：本地、全局
### 本地安装
	npm install jquery 
	本地安装 会在当前目录下创建/node_modules/
	文件夹 安装的内容会放到这个目录下面

### 全局安装 
	npm install http-server -g
	c:/用户/Administrator/AppData/Roaming/npm

### 卸载
	卸载本地包  npm uninstall 模块名
	***  进入要卸载的包的那个目录名

	卸载全局包  npm uninstall http-server -g 模块名

### 更新模块
	更新模块 npm update     模块名
			 npm update -g  模块名 

	packe.json

安装less
压缩css插件	  less-plugin-clean-css






框架less
response.less  
	@import "var.less";
	.pad(@padding){
		padding-left:@padding;
		padding-right:@padding;
	}
	.container{
		&{
			.pad(@padding);
		}
		&-fluid{

		}
		& .row,&-fluid .row{
			margin-left:-@padding;
			right
			height:auto;
		}
		& .row:after,&-fluid .row:after{
			content: "";
			display: block;
			height: 0;
			line-height: 0;
			clear: both;
		}
	}


.grid(@type,@i:1) when (@i<=@cols){
	.col-@{type}-@{i}{
		width:100%/@cols*@i;
		display:block;
		float:left;
		.pad(@padding);
	}
	.grid(@type,@i+1);	
}




<!-- 手机端的栅格 -->
.grid()
<!-- 手机端的栅格 -->

.g(@width,@name){
	@media screen and (min-width: @width){
		.container{
			width:@width - @padding * 2;
		}
		.grid(@name);
	}
}






<!-- >768  平板的栅格 -->


.g(sm,);





var.less
	1.屏幕的阈值
		smscreen 768
		mdscreen 1000
		lgscreen 1200
	2.栅格数量
	cols 12
	3.列间距
	padding 15px





