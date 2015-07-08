video元素的全屏播放
Safari不支持全屏播放API，即使是iOS8也不例外。但是能通过一个特殊的方法解决这个问题，在<video>元素中增加一段js。
<input type="button" value="Go Full screen"  onclick='document.querySelector("video").webkitEnterFullScreen()'>
