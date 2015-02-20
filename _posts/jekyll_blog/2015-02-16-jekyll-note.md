---
layout: post
title: jekyll添加多说评论
category: jekyll
tags: [jekyll]
---
{% include JB/setup %}
用[jekyll-bootstrap](http://jekyllbootstrap.com)搭建的博客默认的评论系统是disqus，而多说更适合国内用户，把disqus换成多说可以先把_config.yml中comments那段设置注释掉，接着修改一个文件。

进入到`_includes/themes/YOUR_THEME_NAME`修改post.html,将\{*% include JB/comments %*\}替换为如下代码

{% highlight html %}

<!-- 多说评论框 start -->
	<div class="ds-thread" data-thread-key="页面ID" data-title="文章标题" data-url="文章网址"></div>
<!-- 多说评论框 end -->
<!-- 多说公共JS代码 start (一个网页只需插入一次) -->
<script type="text/javascript">
var duoshuoQuery = {short_name:"codedcat"};
	(function() {
		var ds = document.createElement('script');
		ds.type = 'text/javascript';ds.async = true;
		ds.src = (document.location.protocol == 'https:' ? 'https:' : 
		'http:') + '//static.duoshuo.com/embed.js';
		ds.charset = 'UTF-8';
		(document.getElementsByTagName('head')[0] 
		 || document.getElementsByTagName('body')[0]).appendChild(ds);
	})();
</script>
<!-- 多说公共JS代码 end -->

{% endhighlight %}
#####然后作一下更改:

1. 页面ID    => **{****{ page.id }****}**
2. 文章标题  => **{****{ page.title }****}**
3. 文章网址  => **{****{ site.production_url }****}****{****{ page.url }****}**

