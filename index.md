---
layout: default.liquid
title: Kookboek
---

<div class="recipe-grid" id="recipeGrid">
{% for post in collections.posts.pages %}
<div class="recipe-card">
<img src="{{ post.data.image }}" class="recipe-image">
<div class="recipe-content">
<h3 class="recipe-title"><a href="{{ post.permalink }}">{{ post.title }}</a></h3>
<div class="recipe-meta">
<span>Voorbereiding: {{ post.data.prep_time }}</span>
</div>
<div class="recipe-meta">
<span>Kook/Bak: {{ post.data.cook_time }}</span>
</div>
<div class="recipe-tags">
{% for tag in post.tags %}
<span class="tag">{{ tag }}</span>
{% endfor %}
</div>
</div>
</div>
{% endfor %}
</div>
