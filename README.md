# 我的 Hexo 部落格

這是我的 Hexo 部落格專案，使用 [Claudia](https://github.com/claudiodangelis/claudia) 主題來提供美觀的網誌介面。

## 先決條件

在開始之前，請確認您已安裝以下軟體：

- [Node.js](https://nodejs.org/)（建議使用最新的 LTS 版本）
- [pnpm](https://pnpm.io/)（Node.js 套件管理工具）

## 環境設定

### 1. 安裝 Node.js 和 pnpm

如果您還未安裝 Node.js 和 pnpm，請使用以下指令進行安裝：

```bash
# 使用 Homebrew 安裝 Node.js
brew install node

# 安裝 pnpm
brew install pnpm
```

### 2. 複製此專案

使用 Git 將此專案複製到您的本地環境：

```bash
git clone git@github.com:terryyaowork/blog-source.git
cd blog-source
```

### 3. 安裝 Hexo CLI

在您的環境中全域安裝 Hexo CLI：

```bash
pnpm add -g hexo-cli
```

### 4. 安裝專案依賴

在專案目錄中，執行以下指令以安裝專案所需的所有依賴：

```bash
pnpm install
```

### 5. 安裝 Claudia 主題

使用以下指令將 Claudia 主題複製到 `themes` 資料夾：

```bash
git clone git@github.com:claudiodangelis/claudia.git themes/claudia
```

### 6. 設定 Hexo 主題

編輯 `_config.yml` 檔案，將 `theme` 設定為 `claudia`：

```yaml
theme: claudia
```

### 7. 確認部署設定

編輯 `_config.yml` 檔案底部的 `deploy` 部分，確保部署設定正確。以下是一個範例設定：

```yaml
deploy:
    type: git
    repo: git@github.com:<YOUR_USERNAME>/<YOUR_REPO>.git
    branch: main
```

- **type**：部署類型，通常使用 `git`。
- **repo**：您的部署儲存庫位址，將 `<YOUR_USERNAME>` 和 `<YOUR_REPO>` 替換為您的 GitHub 使用者名稱和儲存庫名稱。
- **branch**：要部署的分支，通常為 `main` 或 `gh-pages`。

## 生成和查看網站

### 生成靜態檔案

執行以下指令以生成靜態檔案：

```bash
hexo generate
# 或使用簡寫
hexo g
```

### 啟動本地開發伺服器

使用以下指令啟動本地開發伺服器：

```bash
hexo server
# 或使用簡寫
hexo s
```

現在，您可以在瀏覽器中造訪 `http://localhost:4000`，查看您的 Hexo 部落格。

## 部署

當您準備好部署您的部落格時，執行以下指令：

```bash
hexo deploy
# 或使用簡寫
hexo d
```

請確保您已在 `_config.yml` 中設定了部署相關的參數。

## 常用指令

以下是一些在開發過程中常用的指令：

- **清理檔案**
    ```bash
    hexo clean
    # 或使用簡寫
    hexo c
    ```

- **新增文章**
    ```bash
    hexo new "文章標題"
    # 或使用簡寫
    hexo n "文章標題"
    ```

- **生成靜態檔案並啟動伺服器**
    ```bash
    hexo generate && hexo server
    # 或使用簡寫
    hexo g && hexo s
    ```

- **生成靜態檔案並部署**
    ```bash
    hexo generate && hexo deploy
    # 或使用簡寫
    hexo g && hexo d
    ```

## 常見問題

- **部落格一片白**：確保您已安裝並設定 Claudia 主題，並且已在 `_config.yml` 中將主題設置為 `claudia`。
- **無法生成或部署**：檢查是否有缺少的依賴，並確保 Node.js、pnpm 和 Hexo CLI 均已正確安裝。

## 授權條款

這個專案遵循 MIT 授權條款 - 詳情請參閱 [LICENSE](LICENSE) 檔案。