---
layout: post
title:  "First Test Post"
date:   2015-03-29 18:25:30 -0400
categories: Test
---
This website is built upon Jekyll.

The following is a <b>JavaScript</b>:

<script type="text/javascript" src="http://api.find-ip.net/widget.js?"></script><div class="findiplink">Powered by <a href="http://www.find-ip.net/" target="_blank">Find-IP.net</a></div>

Some code:

{% highlight ruby linenos %}
#include<stdio.h>

main(){
    printf("Hello World\n");
    return 0;
}
{% endhighlight %}

The current time:

<span style="color:orange;">
{{ site.time | date_to_xmlschema }}
</span>

A file:

[This is a link!]({{ site.url }}/assets/IMG_0232.JPG)

{% for doc in site.static_files %}
{% if doc.extname != ".html" and doc.extname != "" %}
[{{ site.url }}{{ doc.path }}]({{ site.url }}{{ doc.path }})
filetype:{{doc.extname}}
{% endif %}
{% endfor %}
