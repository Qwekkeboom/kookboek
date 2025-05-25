---
layout: default.liquid
title: Kookboek
---

{% assign categories = collections.posts.pages | map: "data" | map: "category" | uniq | sort %}

{% for category in categories %}
<h2>{{ category | capitalize }}</h2>
<div class="recipe-grid">
{% for post in collections.posts.pages %}
{% if post.data.category == category %}
<div class="recipe-card">
<div class="recipe-content">
<h3 class="recipe-title"><a href="{{ post.permalink }}">{{ post.title }}</a></h3>
<div class="recipe-meta">
<span>{{ post.data.description }}</span>
</div>
<div class="recipe-tags">
{% for tag in post.tags %}
<span class="tag tag-{{ tag | downcase }}">{{ tag }}</span>
{% endfor %}
</div>
</div>
</div>
{% endif %}
{% endfor %}
</div>
{% endfor %}