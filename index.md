---
layout: default
title: Home
---

# Welcome to My Technical Blog

Hi, I'm Lucain Pan, and this is where I share my technical reports, thoughts, and insights about software development and technology.

## Latest Posts

<div class="posts">
  {% for post in site.posts limit:5 %}
    <article class="post">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">
        {{ post.date | date: "%B %d, %Y" }}
      </time>
      <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
    </article>
  {% endfor %}
</div>

## About This Blog

This blog focuses on:
- Technical reports and analyses
- Software development insights
- Programming tips and best practices
- Technology trends and thoughts
- Personal projects and experiments

<div class="navigation-links">
  <a href="{{ '/about' | relative_url }}">About Me</a> |
  <a href="{{ '/posts' | relative_url }}">All Posts</a> |
  <a href="{{ '/feed.xml' | relative_url }}">RSS Feed</a>
</div>
