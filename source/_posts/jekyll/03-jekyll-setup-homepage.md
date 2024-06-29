---
title: "[jekyll] 03 設定首頁的內容"
date: 2024-06-23
categories: [blog]
tags: [jekyll]
---

以下是設定 Jekyll 首頁內容的步驟：

1. **修改 `_config.yml`**：
    確保您的 `_config.yml` 中有以下設置：

    ```yaml
    paginate: 5
    paginate_path: "/page:num/"
    ```

2. **創建首頁模板**：
    在 `_layouts` 目錄中創建一個 `home.html` 文件，並添加以下內容：

    ```html
    ---
    layout: default
    ---

    <div class="home">
        <h1 class="page-heading">{{ page.title | escape }}</h1>
        <ul class="post-list">
        {% for post in paginator.posts %}
            <li>
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            <h2>
                <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            </h2>
            </li>
        {% endfor %}
        </ul>
        <div class="pagination">
        {% if paginator.previous_page %}
            <a class="pagination-item older" href="{{ paginator.previous_page_path | relative_url }}">&larr; Older</a>
        {% endif %}
        {% if paginator.next_page %}
            <a class="pagination-item newer" href="{{ paginator.next_page_path | relative_url }}">Newer &rarr;</a>
        {% endif %}
        </div>
    </div>
    ```

3. **更新首頁文件**：
    確保您的 `index.md` 文件中有以下內容：

    ```markdown
    ---
    layout: home
    title: "首頁"
    permalink: /
    ---
    ```

完成以上步驟後，您的 Jekyll 首頁就會顯示最新的文章列表！
