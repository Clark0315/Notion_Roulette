# 🎯 Notion Roulette

一個可以嵌入到 Notion 的互動輪盤網頁，輪盤項目來源於 JSON 檔案。

## 📺 線上展示

**GitHub Pages:** https://clark0315.github.io/Notion_Roulette/

## ✨ 功能特色

- 🎨 美觀的 SVG 圓形輪盤設計
- 🎲 隨機旋轉動畫（4 秒）
- 💫 停止時的抖動效果
- 📱 響應式設計（支援手機與桌面）
- 🔄 從 JSON 動態載入項目
- 🎯 可完美嵌入 Notion

## 🚀 使用方式

### 在 Notion 中嵌入

1. 在 Notion 頁面中輸入 `/embed`
2. 貼上以下網址：
   ```
   https://clark0315.github.io/Notion_Roulette/
   ```
3. 調整 iframe 大小（建議至少 600x700px）

### 自訂輪盤項目

編輯 `items.json` 檔案來自訂輪盤項目：

```json
[
  { "name": "選項 1", "enabled": true, "color": "#FF6384" },
  { "name": "選項 2", "enabled": true, "color": "#36A2EB" },
  { "name": "選項 3", "enabled": true, "color": "#FFCE56" },
  { "name": "選項 4", "enabled": true, "color": "#4BC0C0" }
]
```

#### 參數說明：
- `name`: 項目名稱
- `enabled`: 是否啟用（`true` 或 `false`）
- `color`: 項目顏色（Hex 色碼）

## 📁 專案結構

```
Notion_Roulette/
├── index.html      # 主要轉盤網頁
├── items.json      # 輪盤項目資料
├── README.md       # 專案說明文件
└── Claude.md       # 專案需求文件
```

## 🛠️ 技術細節

- 純 HTML/CSS/JavaScript（無需框架）
- 使用 SVG 繪製輪盤
- CSS3 動畫與過渡效果
- Fetch API 載入 JSON 資料
- 支援從 GitHub Raw URL 或本地載入資料

## 📝 開發筆記

此專案使用 Claude Code 協助開發，詳細需求請參考 `Claude.md`。

## 🎮 如何修改

1. Fork 此專案
2. 編輯 `items.json` 添加你的項目
3. 提交變更並推送到 GitHub
4. 在 Notion 中使用你的 GitHub Pages 網址

## 📄 授權

MIT License

---

⚡ Made with Claude Code