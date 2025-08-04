---
layout: default
---

<div id="home-content">
  <h1>{{ site.title }}</h1>
  <p>{{ site.description }}</p>
  
  <div id="posts-list">
    {% for post in site.posts %}
      <article class="post-preview">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
        <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      </article>
    {% endfor %}
  </div>
</div>
