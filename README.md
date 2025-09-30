# 🎯 Notion Roulette

一個可以嵌入到 Notion 的互動輪盤網頁，輪盤項目來源於 JSON 檔案。

## 📺 線上展示

**GitHub Pages:** https://clark0315.github.io/Notion_Roulette/

## ✨ 功能特色

- 🎨 美觀的 SVG 圓形輪盤設計
- 🎲 隨機旋轉動畫（4 秒）+ 抖動效果
- 🎯 精準的指針指向與結果計算
- 📱 響應式設計（支援手機與桌面）
- 🔄 從 JSON 動態載入項目
- 🎰 **隨機選擇功能**：從多個項目中隨機挑選指定數量顯示
- 📊 **動態數量調整**：可自訂每次顯示幾個項目
- 💡 可完美嵌入 Notion

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
{
  "displayCount": 6,
  "items": [
    { "name": "A書", "enabled": true, "color": "#FF6384" },
    { "name": "B書", "enabled": true, "color": "#36A2EB" },
    { "name": "C書", "enabled": true, "color": "#FFCE56" },
    { "name": "D書", "enabled": true, "color": "#4BC0C0" },
    { "name": "E書", "enabled": true, "color": "#9966FF" },
    { "name": "F書", "enabled": true, "color": "#FF9F40" },
    { "name": "G書", "enabled": true, "color": "#FF6384" },
    { "name": "H書", "enabled": true, "color": "#4BC0C0" },
    { "name": "I書", "enabled": true, "color": "#FFCE56" },
    { "name": "J書", "enabled": true, "color": "#36A2EB" }
  ]
}
```

#### 參數說明：
- `displayCount`: 每次隨機顯示的項目數量（例如：從 10 本書中隨機選 6 本）
- `items`: 所有可用的項目清單
  - `name`: 項目名稱
  - `enabled`: 是否啟用（`true` 或 `false`）
  - `color`: 項目顏色（Hex 色碼）

#### 使用範例：

**範例 1：調整顯示數量**
```json
{
  "displayCount": 4,  // 從 10 本書中隨機選 4 本
  "items": [...]
}
```

**範例 2：停用某些項目**
```json
{
  "displayCount": 6,
  "items": [
    { "name": "A書", "enabled": false, "color": "#FF6384" },  // 不會被選中
    { "name": "B書", "enabled": true, "color": "#36A2EB" }
  ]
}
```

**範例 3：支援舊格式（向下相容）**
```json
[
  { "name": "選項 1", "enabled": true, "color": "#FF6384" },
  { "name": "選項 2", "enabled": true, "color": "#36A2EB" }
]
```

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
- CSS3 動畫與過渡效果（含 shake 動畫）
- CSS 變數動態控制動畫
- Fetch API 載入 JSON 資料
- 支援從 GitHub Raw URL 或本地載入資料
- Fisher-Yates 洗牌演算法實現隨機選擇
- 精確的角度計算與指針定位

## 🎮 功能說明

### 隨機選擇機制
每次載入頁面時，系統會：
1. 從 `items.json` 讀取所有 `enabled: true` 的項目
2. 根據 `displayCount` 設定，隨機選擇指定數量的項目
3. 重新整理頁面會得到不同的組合

### 旋轉機制
- 旋轉 5-8 圈（隨機）
- 旋轉時間：4 秒
- 停止後抖動：0.9 秒（3 次抖動）
- 指針位於 12 點鐘方向（正上方）
- 結果計算基於指針指向的扇形區域

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