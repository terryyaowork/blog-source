---
layout: page
title: "tags"
permalink: /tags/
---

<div id="tags">
  <ul>
    {% for tag in site.tags %}
      <li>
        <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/">{{ tag[0] }}</a> ({{ tag[1].size }})
      </li>
    {% endfor %}
  </ul>
</div>
