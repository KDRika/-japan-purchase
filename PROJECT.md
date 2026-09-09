# 日本代購 V5

## 版本重點
- 淺棕／奶油白質感 UI
- IndexedDB 大容量資料儲存
- 自動偵測並搬移 V4 `localStorage` 資料
- 可匯入 V4 / V5 JSON 備份
- 商品參考圖與發票皆支援多張
- 圖片可全螢幕查看、縮放、前後切換
- 圖片上傳自動壓縮
- 備份頁顯示瀏覽器儲存空間估計
- CSP 保持 `connect-src 'none'`，不主動向外部 API 傳資料

## 升級步驟
1. 保留 V4 匯出的 JSON 備份。
2. 將 V5 六個檔案覆蓋 GitHub Repository 根目錄。
3. GitHub Pages 自動重新部署。
4. 首次打開 V5：若 IndexedDB 為空，會自動讀取同網域 V4 `localStorage` 並搬移。
5. 若自動搬移未成功，進入「備份資料」匯入 V4 JSON 備份。
