iwant项目中遇到，在安卓webview下，
当使用Backbone event代理 绑定tap 来更改loactionn.href 触发自定义的xxx://
客户端无法捕捉
解决方案：绑定源生click事件，并引入fastclick来加速点击。