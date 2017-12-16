---
title: "Speekenbrink lab - blog"
layout: default
permalink: /blog/
---

<div class="row">

  <h1>Posts</h1>

  <ul class="posts">
    {% for post in site.posts %}
      <li><span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span> <a class="post-link" href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/feed.xml">via RSS</a></p>

</div>
