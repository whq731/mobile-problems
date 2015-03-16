在做iwant评论窗口时遇到的bug
IOS fixed 的元素内包含一个textarea 
当点击输入框时 整个fixed的浮层会被系统冻结 然后下沉了一下
应该是IOS系统对输入框自动居中功能所引起的

解决方案:
改为absloute 弹出时动态设定位置
$(".publish_panel").css("top",window.scrollY + "px").show();

点击输入框时 延迟触发fix top
  $(".publish_content").off().on("click", function () {
                            setTimeout(function(){
                                $(".publish_panel").css("top",window.scrollY + "px");
                            },100);
