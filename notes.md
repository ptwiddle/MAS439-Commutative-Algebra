---
layout: page
title: Notes
permalink: /Notes/
---

This page contains links to the lecture notes for the course.


[Notes from last year's course](../MAS439LastYear.pdf).  The plan is to follow these fairly closely, with some minor changes.  I will try to alert you to any larger changes. 

Each day of lecture will have its own blogpost page.  This should be handy to read on mobile devices, and will have a comment thread to ask questions and further discuss the material.


{% for lecture in site.lecturenotes %}
 - <a href="{{ lecture.url | prepend:site.baseurl }}"> {{ lecture.title }}</a>
{% endfor %} 

