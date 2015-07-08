最开始是使用绑定Input事件 触发调用$.trim回填到input

当输入法为中文时 出现Bug
中文输入发存在一个拼音到汉字的转换过程
当输入拼音时 同样触发Input 导致回调后出现重复字符

最后降级为 失去焦点时 去掉所有空格
on("blur",function(){
//去掉输入的空格
target.val(target.val().replace(/\s/g,""));
});

