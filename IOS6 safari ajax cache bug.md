http://stackoverflow.com/questions/12506897/is-safari-on-ios-6-caching-ajax-results/12516555#

H5结算修改地址 后再次请求返回的地址列表为上次时的
最后在ajax参数里加入一个new Date()的timestamp
保证每次请求的参数不一样即可