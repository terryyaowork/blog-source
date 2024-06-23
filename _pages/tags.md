---
layout: page
title: "tags"
permalink: /tags/
---

<div class="tags">
    <ul class="tag-list">
    {% for tag in site.tags %}
        <li>
        <a href="{{ site.baseurl }}/tags/{{ tag | first }}">{{ tag | first }}</a> ({{ tag | last | size }})
        </li>
    {% endfor %}
    </ul>
</div>
