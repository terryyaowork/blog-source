---
title: "[jekyll] 04 設定分類和 Tags 頁面的內容"
date: 2024-06-23
categories: [blog]
tags: [jekyll]
---

以下是設定 Jekyll 分類和 Tags 頁面內容的步驟：

1. **創建分類頁面**：
    在 `_pages` 目錄中創建一個 `categories.md` 文件，並添加以下內容：

    ```markdown
    ---
    layout: page
    title: "分類"
    permalink: /categories/
    ---

    <div class="categories">
        <h1>{{ page.title }}</h1>
        <ul class="category-list">
        {% for category in site.categories %}
            <li>
            <a href="{{ site.baseurl }}/categories/{{ category | first }}">{{ category | first }}</a> ({{ category | last | size }})
            </li>
        {% endfor %}
        </ul>
    </div>
    ```

2. **創建 Tags 頁面**：
    在 `_pages` 目錄中創建一個 `tags.md` 文件，並添加以下內容：

    ```markdown
    ---
    layout: page
    title: "Tags"
    permalink: /tags/
    ---

    <div class="tags">
        <h1>{{ page.title }}</h1>
        <ul class="tag-list">
        {% for tag in site.tags %}
            <li>
            <a href="{{ site.baseurl }}/tags/{{ tag | first }}">{{ tag | first }}</a> ({{ tag | last | size }})
            </li>
        {% endfor %}
        </ul>
    </div>
    ```

3. **更新 `_config.yml`**：
    確保您的 `_config.yml` 文件中有以下設置：

    ```yaml
    header_pages:
        - about.md
        - index.md
        - posts.md
        - categories.md
        - tags.md
    ```

完成以上步驟後，您的 Jekyll 站點就會顯示分類和 Tags 頁面。
