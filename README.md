Fy
==

一个纯JavaScript分页插件

任何人都可以免费使用、修改、发布

author:oospace

email:oospace@foxmail.com


使用方法
==

代码前几行进参数配置


//总条数(必填)     
var Num=Number(<?php echo $count;?>)     
//当前页(必填)     
var index = Number(<?php echo $page;?>);    
//每页的条数(可选,默认每页10条) 
var  pageNum=Number(10);       
//最大显示的页码的数目(可选，默认显示5个页码,页码数目必须大于等于1) 
var  maxPageNum=Number(5);

控制分页位置及分页显示的设置


//分页区域填写     
$('.page').html(str);     //不使用JQuery时，document.getElementById("page").html(str);
<table class="page" id="page">    
<tr><td>此处分页只需要传递给我当前页码和总页数即可</td></tr>     
</table>

分页提交页码查询事件


function submit(pageIndex) {         
//var sortInfo = $.getUrlParam('sortInfo');//判断是哪一个页面的查询         
var url = "<?php echo current_url();?>?page="+pageIndex+"&field=<?php echo$field;?>&value=<?php echo $field_value;?>";  window.location.href=url;    
}



