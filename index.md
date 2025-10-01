---
layout: default
title: Index
---


# /index


Welcome to **Unlogical Organisms** — a smol‑web notebook maintained by an old nerd. Everything is Markdown. New posts show up here automatically.


## latest


{% assign posts = site.posts %}
{% for post in posts %}
- {{ post.date | date: "%Y-%m-%d" }} · [{{ post.title }}]({{ post.url }})
{% if post.excerpt %}
<span class="excerpt">{{ post.excerpt | strip_html | truncate: 220 }}</span>
{% endif %}
{% endfor %}