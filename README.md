# 桐House一家・家庭旅行手帳 PWA v6.4

## iPhone 搬家檔相容性修正
v6.3 使用 `.tonghouse` 自訂副檔名。iPhone「檔案」App 雖然看得到，但 Safari/PWA 的檔案選擇器可能不把它視為可選檔案。

v6.4 改成標準 `.json`：
- 檔名：`桐House一家_完整搬家_YYYY-MM-DD.json`
- MIME：`application/json`
- iPhone Safari / PWA 檔案選擇器可正常辨識。
- 備份內容與 v6.3 一樣完整，照片仍以 Base64 存在 JSON 內，不會因改成 `.json` 而遺失。
- 搬入仍採安全合併：相同住宿 ID 更新，不同 ID 都保留。

## 建議測試
1. 舊 iPhone 使用 v6.4 → 工具 → 📤 搬出手札。
2. AirDrop 新產生的 `.json` 到新 iPhone。
3. 新 iPhone 開桐House v6.4 → 工具 → 📥 搬入手札。
4. 在「檔案」App 選 AirDrop 收到的 `桐House一家_完整搬家_日期.json`。
5. 確認住宿筆數、備註與照片。

## 舊 `.tonghouse`
iOS 可能無法從網頁檔案選擇器選取。請在舊手機重新用 v6.4 匯出一份 `.json`，不要再使用舊 `.tonghouse` 檔。
