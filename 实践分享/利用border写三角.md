京东这么写的
.tab-arrow {
position: absolute;
z-index: 1;
top: 23px;
left: 0;
height: 7px;
border-bottom: 2px solid #E4393C;
overflow: hidden;
text-align: center;
}
.tab-arrow b {
display: inline-block;
margin-top: -8px;
width: 0;
height: 0;
border-style: dashed dashed solid;
border-width: 10px;
border-color: transparent transparent #E4393C;
overflow: hidden;
zoom: 1;
font-size: 0;
	}
<div class="tab-arrow" style="left: 632px;">
<b></b>
</div>
	
	
	
----------------------------------------------------
利用css中的border生成三角，兼容包括IE6的主流浏览器
	
	来自 <http://www.36ria.com/demo/triangle/> 
	
http://www.jb51.net/css/33742.html




上下翻转箭头

.rarrow_block{
    position: relative;
	display: inline-block;
	-webkit-background-size: 22px 9px!important;
	width: 22px;
	height: 9px;
}
.rarrow_block em{
    position: absolute;
    top: 2px;
    left: 0;
    width: 0;
    height: 0;
    border-color:  rgba(255, 255, 255, 0);
    border-top-color: #CBCBCB;
    border-style: solid;
    overflow: hidden;
    border-width: 8px 8px 0;
} 
.rarrow_block span{
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 0;
    border-color: rgba(255, 255, 255, 0);
    border-top-color: #fff;
    border-style: solid;
    overflow: hidden;
    border-width: 8px 8px 0;
} 
.rarrow_block_down{
    margin-bottom: -2px;
}
.rarrow_block_down em{
    position: absolute;
    top: -2px;
    left: 0;
    width: 0;
    height: 0;
    border-color: rgba(255, 255, 255, 0);
    border-bottom-color: #CBCBCB;
    border-style: solid;
    overflow: hidden;
    border-width: 0 8px 8px;
} 
.rarrow_block_down span{
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 0;
    border-color:  rgba(255, 255, 255, 0);
    border-bottom-color: #fff;
    border-style: solid;
    overflow: hidden;
    border-width: 0 8px 8px;
} 





