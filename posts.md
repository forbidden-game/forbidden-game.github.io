---
layout: page
title: All Posts
permalink: /posts/
---

# All Posts

Here's a complete list of all my blog posts, organized by date:

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <div class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%B %d, %Y" }}
        </time>
        {% if post.tags %}
          <div class="post-tags">
            {% for tag in post.tags %}
              <span class="tag">{{ tag }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
      <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
    </article>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
  <p>No posts yet. Check back soon for new content!</p>
{% endif %}

---

Want to stay updated? Subscribe to the [RSS feed]({{ '/feed.xml' | relative_url }}) to get notified of new posts.
