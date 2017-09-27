---
layout: page
title: Bulletins
permalink: /Bulletins/
---


Every week will have a short webpage called a bulletin, with a short description of the mathematics that was covered that week, any administrative anouncements, copies of any slides used, links to any supplementary sources, and perhaps a link or two of general interest.  Each bulletin also contains a comment section for any discussions of that week.  


<ul>
{% for bulletin in site.bulletins %}
<li>
<a href="{{ bulletin.url | prepend:site.baseurl }}"> {{ bulletin.title }}</a>
</li>
{% endfor %}
