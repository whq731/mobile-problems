页面过长时,快速下拉,页面迅速滚动底部
此时window.pageYoffset会不准确
导致使用position:fixed的元素的实际位置和显示位置发生偏移
出现“看得见，摸不着的情况(触摸不到绑定事件的区域来触发事件)”

解决：
强制滚动到页首
或者让用户点击下页面
触发页面reflow即可