---
title: Hexo 基本設置
date: 2024-08-05 23:33:33
categories: [hexo]
tags: [hexo]
---

# Hexo 基本設定指南

這份文件將帶您了解如何在本機環境中安裝和設定 Hexo，以便開始建立您的靜態部落格網站。

## 先決條件

在開始之前，請確認您已安裝以下軟體：

- [Node.js](https://nodejs.org/)（建議使用最新的 LTS 版本）
- [pnpm](https://pnpm.io/)（Node.js 套件管理工具）

## 安裝 Hexo

### 1. 安裝 Node.js 和 pnpm

如果您還未安裝 Node.js 和 pnpm，請使用以下指令安裝：

```bash
# 使用 Homebrew 安裝 Node.js
brew install node

# 安裝 pnpm
brew install pnpm
```

### 2. 全域安裝 Hexo CLI

使用 pnpm 全域安裝 Hexo CLI：

```bash
pnpm add -g hexo-cli
```

### 3. 初始化 Hexo 專案

選擇一個目錄來存放您的部落格專案，然後使用以下指令初始化 Hexo 專案：

```bash
mkdir my-blog
cd my-blog
hexo init
```

接下來，安裝專案所需的依賴：

```bash
pnpm install
```

## 基本配置

Hexo 的基本配置檔案是根目錄下的 `_config.yml`，以下是一些常見的設定：

### 網站基本信息

在 `_config.yml` 中設定網站的基本信息：

```yaml
title: My Blog
subtitle: Welcome to my blog
description: 這是一個使用 Hexo 建立的部落格
author: 您的名稱
language: zh-TW
```

### 設定網址

設定部落格的 URL：

```yaml
url: https://您的域名.com
root: /
permalink: :year/:month/:day/:title/
```

### 設定佈局

選擇部落格的主題（佈局樣式）：

```yaml
theme: claudia
```

要使用特定主題，例如 Claudia，您需要先將主題安裝到 `themes` 資料夾：

```bash
git clone git@github.com:claudiodangelis/claudia.git themes/claudia
```

### 部署設定

設定如何將網站部署到伺服器：

```yaml
deploy:
    type: git
    repo: git@github.com:<YOUR_USERNAME>/<YOUR_REPO>.git
    branch: gh-pages
```

請將 `<YOUR_USERNAME>` 和 `<YOUR_REPO>` 替換為您的 GitHub 使用者名稱和倉庫名稱。

## 常用指令

以下是一些常用的 Hexo 指令，幫助您在開發過程中更有效率：

- **清理檔案**

    清除暫存檔和生成的檔案：

    ```bash
    hexo clean
    # 或使用簡寫
    hexo c
    ```

- **生成靜態檔案**

    生成網站的靜態檔案：

    ```bash
    hexo generate
    # 或使用簡寫
    hexo g
    ```

- **啟動本地開發伺服器**

    啟動本地伺服器以預覽網站：

    ```bash
    hexo server
    # 或使用簡寫
    hexo s
    ```

    現在，您可以在瀏覽器中造訪 `http://localhost:4000`。

- **部署網站**

    部署網站到遠端伺服器：

    ```bash
    hexo deploy
    # 或使用簡寫
    hexo d
    ```

- **新增文章**

    新增一篇新文章：

    ```bash
    hexo new "文章標題"
    # 或使用簡寫
    hexo n "文章標題"
    ```

## 部署網站

Hexo 支援多種部署方式，這裡以 GitHub Pages 為例：

1. 確認 `_config.yml` 中的 `deploy` 部分已正確設定。
2. 執行以下指令以生成並部署網站：

    ```bash
    hexo generate --deploy
    # 或使用簡寫
    hexo g -d
    ```

這將自動生成靜態檔案並將它們推送到您設定的 GitHub 倉庫中。

## 常見問題

- **部落格一片空白**：確認主題已正確安裝，並在 `_config.yml` 中設定 `theme`。
- **無法生成或部署**：確認是否有安裝錯誤的依賴，並確保 Node.js 和 Hexo CLI 均已正確安裝。

## 授權條款

這個專案遵循 MIT 授權條款 - 詳情請參閱 [LICENSE](LICENSE) 檔案。