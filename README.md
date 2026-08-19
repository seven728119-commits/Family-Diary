# 桐House一家・家庭旅行手帳 PWA v6.3

## 這版修正：GitHub Pages 更新後 iPhone 還看到舊版
v6.2 的 Service Worker 對 `index.html` 採 cache-first，因此 iPhone 已加入主畫面的 PWA 可能一直顯示舊版。

v6.3 改為：
- 網頁 / `index.html`：network-first，先抓 GitHub Pages 最新版。
- 離線時：才退回快取版。
- 圖示 / manifest 等靜態資源：仍可使用快取。
- 新 Service Worker 安裝後 `skipWaiting()` + `clients.claim()`，較快接管舊版本。
- 保留 v6.2 的「📤 搬出手札 / 📥 搬入手札」完整搬家功能。

## 第一次從舊版升級
若手機仍被舊 Service Worker 卡住：
1. 先用 Safari 直接開 GitHub Pages 網址，不要從主畫面 App 開。
2. 重新整理頁面一次。
3. 關掉 Safari 與主畫面 App，再重新開啟。
4. 若仍沒變，iPhone：設定 → Safari → 進階 → 網站資料 → 找到 github.io / 對應網站，刪除網站資料後再開。
   注意：刪除網站資料也會清掉 localStorage，所以請先在舊版用「搬出手札」做完整備份。
