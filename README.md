# 桐House一家 v6.8.1｜資料救援版

這版只處理資料安全，不新增功能。

## 啟動時
1. 優先讀取固定資料 key：`hotel_memories_v1`。
2. 如果這個 key 沒有有效住宿紀錄，會掃描同一 GitHub Pages 網址下的其他 localStorage 項目。
3. 找到舊版住宿陣列或完整備份格式時，會複製回 `hotel_memories_v1`。
4. 不刪除舊 key，保留原資料作為安全退路。
5. 完全停用 sample/demo 自動資料，避免空畫面時建立範例紀錄而掩蓋資料問題。
6. 成功救回時會顯示「找回 X 筆原本的旅行紀錄」。

## 重要
請部署在「原本完全相同的 GitHub Pages 網址 / origin」。
localStorage 是依網站來源隔離的；如果換 repo、換網址、換 domain，新網址無法直接讀到舊網址的 localStorage。
若舊資料已被瀏覽器網站資料清除，則需使用先前匯出的 JSON 完整搬家檔恢復。
