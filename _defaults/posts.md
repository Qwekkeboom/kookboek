---
title: Recipe Title
layout: default.liquid
data: {
  category: Dinner,
  prep_time: 15 min,
  cook_time: 30 min,
  description: A short description about the recipe
}
tags:
  - Tag 1
  - Tag 2
is_draft: true
---

# {{ page.title }}

Voorbereidingstijd: {{ page.data.prep_time }} | Kook- of baktijd: {{ page.data.cook_time }}

## Ingrediënten
- Ingredient 1
- Ingredient 2
- Ingredient 3

## Bereiding
1. Step one
2. Step two
3. Step three