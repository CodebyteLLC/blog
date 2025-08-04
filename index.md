---
layout: default
---

<div id="home-content">
  <h1>{{ site.title }}</h1>
  <p>{{ site.description }}</p>
  
  <div id="posts-list">
    {% for post in site.posts %}
      <article class="post-preview">
        {% if post.image %}
          <img 
             src="{{ post.image | relative_url }}" 
             alt="{{ post.title }}" 
            class="post-thumbnail" 
            style="width: 130px; height: auto;"
          >
        {% endif %}
        <p class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></p>
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
        <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      </article>
    {% endfor %}
  </div>
</div>
