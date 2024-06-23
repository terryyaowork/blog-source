---
layout: page
title: "tags"
permalink: /tags/
---

<h2>標籤列表</h2>
<div id="tags">
  <ul>
        {{ site.tags | jsonify }}
    {% for tag in site.tags %}
      <li>
        <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/">{{ tag[0] }}</a> ({{ tag[1].size }})
      </li>
    {% endfor %}
  </ul>
</div>

<h2>調試輸出</h2>
<div>
  {% for tag in site.tags %}
    <p>{{ tag[0] }}: {{ tag[1] | size }} 篇文章</p>
  {% endfor %}
</div>
