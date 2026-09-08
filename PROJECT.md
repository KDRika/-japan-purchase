# 日本代購 App

## 目前版本
V3 Secure — 手機優先 PWA。

## 已完成功能
- 新增、編輯、刪除代購品項
- 商品名稱、委託人、店家分類、數量、狀態、日幣金額、備註
- 商品參考圖可多張上傳，後續追加不會覆蓋舊照片
- 發票照片可多張上傳，後續追加不會覆蓋舊照片
- 商品與發票照片縮圖可點開全螢幕查看
- 照片檢視器支援上一張／下一張、放大／縮小／重設
- 編輯時可單獨刪除某一張商品或發票照片
- 舊版單張 receipt 資料會自動轉成 receiptImages 陣列
- 搜尋、依委託人、依店家、發票紀錄
- 每位委託人日幣結算
- JSON 完整備份／還原
- PWA manifest、App icon、離線 Service Worker
- CSP：禁止 App 對外發起 API / WebSocket 連線
- 圖片先在裝置端壓縮後存入 localStorage

## 資料安全模型
資料只儲存在目前瀏覽器的 localStorage；GitHub Pages 僅提供 App 程式碼，不儲存使用者代購資料或照片。App 的 CSP 使用 `connect-src 'none'`，禁止主動對外傳送資料。

## 部署
GitHub Pages：main branch / root。
更新 index.html 或 sw.js 後重新提交，Service Worker cache key 已更新為 `jp-purchase-v3-secure`，以避免手機持續使用舊版快取。
