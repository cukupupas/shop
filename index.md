---
layout: default
title: Home
---

<h1>Welcome to My Shop</h1>
<ul>
{% for product in site.data.products %}
  <li>
    <a href="{{ product.name | slugify | prepend: '/products/' | relative_url }}">{{ product.name }}</a>
    <p>{{ product.description }}</p>
    <p>Price: ${{ product.price }}</p>
    <img src="{{ product.image }}" alt="{{ product.name }}">
  </li>
{% endfor %}
</ul>

