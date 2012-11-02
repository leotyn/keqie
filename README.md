关于渴切css框架
keqiecss（渴切商用css框架）前身是thinkcss。是一个 (X)HTML/CSS 框架 ,它的目的是减少你的css开发时间。它提供一个可靠的css基础去创建你的项目,能够用于网站的快速设计,通过重设和重建浏览器标准，可以让每个网站防止枯燥的跨浏览器兼容性测试。你可以将他理解成一套模板，里面包含了大多数站点中所需要的那些css类。他很小，只有四个文件而已。总共不到6KB。

渴切css之重写

    body{ color:#000000; font-family:Verdana, Arial, Helvetica, sans-serif;}
     
     * {}
     a{outline:none; text-decoration:none;} a:hover{ text-decoration:underline;}
     html{zoom:1;}html *{outline:0;zoom:1;} html button::-moz-focus-inner{border-color:transparent!important;} 
     body{overflow-x: hidden; font-size:12px;} body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{margin:0;padding:0;} table{/*border-collapse:collapse;border-spacing:0;*/} fieldset,a img{border:0;} address,caption,cite,code,dfn,em,th,var{font-style:normal;font-weight:normal;} li{list-style:none;} caption,th{text-align:left;} h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal;} q:before,q:after{content:'';}

渴切css之清除浮动

.clearfix:after {content:"."; display:block; height:0; clear:both; visibility:hidden; }.clearfix {display:block;}.clear{ clear:both;}/* 清除浮动*/

渴切css之ie6透明

/*png图片ie6下透明滤镜实现写法*/
 .pngimg{filter: progid:DXImageTransform.Microsoft.AlphaImageLoader(enabled=true, sizingMethod=scale, src='images/x.png');}

渴切css之透明度

.transparent{filter:alpha(opacity=50); -moz-opacity:0.5;/** Firefox 3.5即将原生支持opacity属性，所以本条属性只在Firefox3以下版本有效 ***/ -khtml-opacity: 0.5; opacity: 0.5; } 

渴切css之固定不动

/* 兼容IE6的定位属性fixed，固定不动样式 */
 .fixed{
   position:fixed; 
 	clip:rect(0 100% 100% 0);
 	_position:absolute;
 	
 	/* 底部 */
 	bottom:0px;
 	left:0px;
 	_top:expression(document.documentElement.scrollTop+document.documentElement.clientHeight-this.clientHeight);
 	/*_left:expression(document.documentElement.scrollLeft + document.documentElement.clientWidth - offsetWidth);*/
 	
 	/* 左侧 */
 	/*left:0px;*/
 	/*_top:expression(document.documentElement.scrollTop+document.documentElement.clientHeight-this.clientHeight);*/
 	/*_left:expression(document.documentElement.scrollLeft + document.documentElement.clientWidth - offsetWidth);*/
 }
 /* 解决固定层在IE6下闪的问题 */
 *html{
 	background-image:url(about:blank);
 	background-attachment:fixed;
 }

更多请浏览：http://www.keqie.com 