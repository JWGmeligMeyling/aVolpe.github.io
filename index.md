---
layout: page
title: Welcome!
tagline: 
---
{% include JB/setup %}

<h1> Posts </h1>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; 
        <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
        <p class="description">
           "{{ post.description | xml_escape}}" in <a href="{{ BASE_PATH }}tags.html#{{ post.category }}-ref">{{ post.category }}</a>
        </p>
        
    </li>
  {% endfor %}
</ul>

