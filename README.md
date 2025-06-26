# n8n LINE Webhook 自動部署

透過 Render 平台一鍵部署 n8n，並與 LINE 官方帳號整合，實現自動回覆「業績報表」！

## 🚀 快速開始

### 一鍵部署到 Render

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/你的帳號/n8n-line-webhook)

### 環境變數設定（Render > Environment）

| 名稱           | 說明                           |
|----------------|--------------------------------|
| `N8N_USER`     | 登入 n8n 的帳號               |
| `N8N_PASSWORD` | 登入 n8n 的密碼               |
| `WEBHOOK_URL`  | Render 部署完成後的網址       |

---

## 🧩 Webhook 整合 LINE Messaging API

1. 在 n8n 中建立 Webhook 節點：
   - Method: `POST`
   - Path: `line`

2. LINE 設定 Webhook URL：
   ```
   https://your-subdomain.onrender.com/webhook/line
   ```

3. 在流程中處理 LINE 的訊息事件，並使用 HTTP Request 回覆訊息

---

## 📦 範本功能

當使用者傳送「業績報表」時，自動查詢資料庫並回覆格式化的報表內容，例如：
```
📆 今日銷售日期：2025/06/26
💰 營收總額：2,222 元
📦 訂單總數：1筆
...
```

---

## ✅ 小提醒

- Render 免費帳號會自動休眠，可考慮升級 Pro 避免延遲
- 若連接外部資料庫，請設定 Render 防火牆白名單

---

## 📄 授權
本專案不可自行使用、修改，用於公司內部自動化開發。
