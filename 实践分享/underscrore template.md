backbone集成了underscrore.
所以可以用_.template();

这个模板方法进行页面上标签和数据的混合
刚接触php，感觉很像
只不过php的服务器自动经行了模板和数据的混合
而对于前端可以这样来调用混合方法


	var template = _.template("hello: <%= name %>");
	 console.log(template({name : "<Way!>"}));
	=> hello: <Way!>
	
	<% = xxxxx   %> 里也可以执行js代码
	
	var list =  "<% _.each(people, function(name) { %> <li><%= name %></li> <% }); %>";
	console.log(_.template(list, {people: ['moe', 'curly', 'larry']}))
	=> "<li>moe</li><li>curly</li><li>larry</li>"
	
	源文档 <http://underscorejs.org/#template> 
	
	
	
使用 - xxx时 进行html转义

	var template = _.template("hello: <%- name %>");
	 console.log(template({name : "<Way!>"}));
	=> hello: &lt;Way!&gt; 
	

源文档 <http://underscorejs.org/#template> 
