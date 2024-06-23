---
layout: page
title: "categories"
permalink: /categories/
---

<div id="categories">
  <ul>
    {% for category in site.categories %}
      <li>
        <a href="{{ site.baseurl }}/categories/{{ category[0] | slugify }}/">{{ category[0] }}</a> ({{ category[1].size }})
      </li>
    {% endfor %}
  </ul>
</div>
