---
layout: post
title: "基本安裝 Jekyll 的流程及啟動"
date: 2024-06-23
categories: jekyll
tags: ["jekyll"]
---

以下是安裝 Jekyll 的基本步驟：

1. **安裝 Jekyll 和 Bundler**：
    在命令行中運行以下命令來安裝 Jekyll 和 Bundler：

    ```bash
    gem install jekyll bundler
    ```

2. **創建新的 Jekyll 站點**：
    運行以下命令來創建一個新的 Jekyll 站點：

    ```bash
    jekyll new myblog
    cd myblog
    ```

3. **安裝依賴項**：
    在新的站點目錄中運行以下命令來安裝所需的依賴項：

    ```bash
    bundle install
    ```

4. **啟動本地服務器**：
    運行以下命令來啟動 Jekyll 本地服務器：

    ```bash
    bundle exec jekyll serve
    ```

5. **訪問本地站點**：
    打開瀏覽器，訪問 `http://localhost:4000` 來查看您的新 Jekyll 站點。

按照以上步驟，您就能夠成功安裝並啟動 Jekyll 站點！
