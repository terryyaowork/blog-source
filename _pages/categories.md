---
layout: page
title: "categories"
permalink: /categories/
---

<div class="categories">
    <ul class="category-list">
    {% for category in site.categories %}
        <li>
        <a href="{{ site.baseurl }}/categories/{{ category | first }}">{{ category | first }}</a> ({{ category | last | size }})
        </li>
    {% endfor %}
    </ul>
</div>
