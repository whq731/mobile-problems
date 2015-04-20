m站购物车
隐藏url地址栏 此时iscroll滑动区域会多出一个灰色区域
需要重新计算下 高度
 $(document).ready(function(){
        cart.init();
        if(document.documentElement.scrollHeight <= document.documentElement.clientHeight) {
        	window.hideurlbar = true;
            var body = document.getElementsByTagName('body')[0];
            body.style.height = document.documentElement.clientWidth / screen.width * screen.height + 'px';
        }
        window.hideurlbar && setTimeout(function() {
        	window.scrollTo(0, 1);
            // header高度始终取不带下拉窗口的原始高度
            var windowHeight = window.innerHeight-$('footer').height() - $(".h_label").height();
            $("#wrapper").height(windowHeight);
            cart.scroller && cart.scroller.refresh();
        }, 
0);


点击数量编辑时 弹出键盘后
吸底浮层 会出现灰色多余区域
需要在弹出键盘时重新计算下整体高度 和滑动区域高度
//当地址栏和工具栏隐藏时重新计算滑动区域高度
   $(window).resize(function(event) {
       var windowHeight = window.innerHeight-$('footer').height() - $(".h_label").height();
            $("#wrapper").height(windowHeight);
            var body = document.getElementsByTagName('body')[0];
            body.style.height = document.documentElement.clientHeight + 'px';
            cart.scroller && cart.scroller.refresh();
   });
   
