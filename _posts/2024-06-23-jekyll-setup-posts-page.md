---
layout: post
title: "設定 /posts/ 頁面的內容"
date: 2024-06-23
categories: jekyll
tags: ["jekyll"]
---

以下是設定 Jekyll `/posts/` 頁面內容的步驟：

1. **創建 posts 頁面**：
    在 `_pages` 目錄中創建一個 `posts.md` 文件，並添加以下內容：

    ```markdown
    ---
    layout: page
    title: "所有文章"
    permalink: /posts/
    ---

    <div class="posts">
        <h1>{{ page.title }}</h1>
        <ul class="post-list">
        {% for post in site.posts %}
            <li>
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            <h2>
                <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            </h2>
            </li>
        {% endfor %}
        </ul>
    </div>
    ```

2. **更新 `_config.yml`**：
    確保您的 `_config.yml` 文件中有以下設置：

    ```yaml
    header_pages:
        - about.md
        - index.md
        - posts.md
    ```

完成以上步驟後，您的 `/posts/` 頁面就會顯示所有的文章列表。
