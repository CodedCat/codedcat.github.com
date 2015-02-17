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


{% endhighlight %}