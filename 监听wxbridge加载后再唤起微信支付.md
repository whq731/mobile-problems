从微信进入支付中心直接唤起微信支付时
有时会抛出ReferenceError：weixinJSBridge is not defined的异常
实际是浏览器加载weixinJSBridge需要一点延迟时间

改为监听ready事件之后再进行下一步操作
if (typeof window.WeixinJSBridge == "undefined"){
    $(document).on('WeixinJSBridgeReady',function(){
        $('#weiXinPay').click();
    });
}else{
    $('#weiXinPay').click();

}