---
layout: page
title: Notes
permalink: /Notes/
---

This page contains links to the lecture notes for the course.

A running pdf of the lecture notes here.

In addition, each day of lecture will have its own blogpost page.  This should be handy to read on mobile devices, and will have a comment thread to ask questions and further discuss the material.


{% for lecture in site.lecturenotes %}
 - <a href="{{ lecture.url | prepend:site.baseurl }}"> {{ lecture.title }}</a>  Date {{ lecture.date }}
{% endfor %} 

