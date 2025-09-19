# 邏輯推理與資訊安全實驗室網站

## 自動部署設置

本專案使用 GitHub Actions 自動部署到 GitHub Pages。

https://NTUT-Lac.github.io/Website/

## 本地開發

### 安裝 Hugo

首先需要安裝 Hugo (建議使用 Extended 版本)：

**Windows:**
```powershell
# 使用 winget
winget install Hugo.Hugo.Extended

```
安裝後請重啟 vscode

其他平台可參考 [Install Hugo](https://gohugo.io/installation/)

### 下載主題

在 LacWeb 目錄下執行以下指令：

```bash
# 初始化並下載 submodule
git submodule init
git submodule update
```

下載後在 themes\hugo-theme-tokiwa 下應該會有主題檔案

### 下載主題
將 hugo.toml 的 baseURL 改為 dev url

### 啟動開發環境

在 LacWeb 目錄下執行以下指令：

```bash
cd LacWeb
hugo server -D
```

啟動後在瀏覽器開啟 http://localhost:1313 即可預覽網站。

## 專案結構

```
.
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions 工作流程
├── LacWeb/                   # Hugo 網站源碼
│   ├── content/              # 網站內容
│   ├── layouts/              # 自定義模板
│   ├── static/               # 靜態資源
│   ├── data/                 # 資料檔案
│   ├── hugo.toml             # Hugo 配置
│   └── themes                # 主題 (請勿更動)
└── origin/                   # 原始靜態檔案（已忽略）
```