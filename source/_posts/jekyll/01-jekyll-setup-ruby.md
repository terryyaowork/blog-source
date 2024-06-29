---
title: "[jekyll] 01 設定 Jekyll 所需要的 Ruby 環境"
date: 2024-06-23
categories: [blog]
tags: [jekyll]
---

要安裝並使用 Jekyll，您需要先設置好您的 Ruby 環境。以下是步驟：

1. **安裝 Ruby**：
    在 macOS 上，您可以使用 Homebrew 來安裝 Ruby：

    ```bash
    brew install ruby
    ```

2. **安裝 Bundler**：
    Bundler 是 Ruby 的包管理器，您可以使用以下命令來安裝：

    ```bash
    gem install bundler
    ```

3. **檢查 Ruby 版本**：
    確保您安裝了正確的 Ruby 版本：

    ```bash
    ruby -v
    ```

4. **設定 PATH**：
    在您的 `.bash_profile` 或 `.zshrc` 中添加以下內容，讓系統找到正確的 Ruby 路徑：

    ```bash
    export PATH="/usr/local/opt/ruby/bin:$PATH"
    ```

完成以上步驟後，您就已經成功設定了 Jekyll 所需要的 Ruby 環境！
