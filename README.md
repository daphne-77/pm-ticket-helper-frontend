# PM 開票小幫手 - 前端

協助 PM 快速產生開發 Ticket 的小工具。

## 檔案結構

```
pm-ticket-helper-frontend/
├── index.html    # 主頁面
├── config.js     # 設定檔（後端 URL）
└── README.md
```

## 設定

部署前請修改 `config.js`：

```javascript
const CONFIG = {
  // 填入你的後端 API 網址
  API_BASE_URL: 'https://your-backend.zeabur.app',
  
  CLAUDE_MODEL: 'claude-sonnet-4-20250514',
  MAX_TOKENS: 4096,
};
```

## GitHub Pages 部署

1. 建立新的 GitHub Repository

2. 上傳檔案：
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

3. 啟用 GitHub Pages：
   - 前往 Repository → Settings → Pages
   - Source 選擇 `main` branch
   - 資料夾選擇 `/ (root)`
   - 點擊 Save

4. 等待部署完成，網址會是：
   `https://your-username.github.io/repo-name/`

## 使用方式

### 方式一：使用後端試用模式
- 確保 `config.js` 已設定正確的後端 URL
- 每日有 3 次免費試用額度

### 方式二：使用自己的 API Key
- 點擊右上角「設定 API Key」
- 輸入你的 Claude API Key
- 不受每日限制

## 功能

- Ticket 類型：功能開發 (feat) / Bug 修復 (fix)
- 截圖文字辨識
- 多語系翻譯（Web 12 種 / App 6 種）
- 一鍵複製 Markdown 格式
