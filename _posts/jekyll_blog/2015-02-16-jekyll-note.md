---
layout: post
title: jekyll添加多说评论
category: jekyll
tags: [jekyll]
---
{% include JB/setup %}
用jekyll-bootstrap搭建的博客默认的评论系统是disqus，而多说更适合国内用户，把disqus换成多说其实只需简单的修改一个文件
 进入到_includes/themes/YOUR_THEME_NAME
修改post.html,将\{
% include JB/comments 
%\}替换为如下代码即可

{% highlight html %}
<div id="comments" class="ds-thread" data-title="\{\{ page.title \}\}" data-url="\{\{ site.production_url \}\}\{\{ page.url \}\}" data-data-thread-key="\{\{ page.id \}\}"></div>
<script type="text/javascript">
var duoshuoQuery = \{short_name:"CodedCat"\};
(function() \{
var ds = document.createElement('script');
ds.type = 'text/javascript';ds.async = true;
ds.src = 'http://static.duoshuo.com/embed.js';
ds.charset = 'UTF-8';
(document.getElementsByTagName('head')[0]
|| document.getElementsByTagName('body')[0]).appendChild(ds);
\})();
</script>
{% endhighlight %}