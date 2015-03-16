	var nav = window.navigator;
	var OSVersion = nav.appVersion.match(/Android (\d+\.\d+)/i);
	if(OSVersion) {
		//2.2和2.3fixed有bug
		if(OSVersion[1] == '2.2' || OSVersion[1] == '2.3') {
			var block = $(".pt_d");
			block.css('position','absolute');
			block.css('margin','0');
			setTimeout(function(){
				block.css('top', window.scrollY + window.innerHeight/2 - block.height()/2 + 'px'); 
			},0);
		}
	}

改为absolute定位到相对于当前窗口的指定位置