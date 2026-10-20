# 虎尾國小學習教室

學生遊戲大廳。首頁會自動列出 `games/` 裡的每個遊戲資料夾。

## 上架規則
- 每個遊戲一個資料夾：`games/<英文名稱>/`
  - `index.html`：最新版遊戲（固定檔名，網址才不會變）
  - `info.json`：首頁卡片資料（name、subject：國語／數學／個別化／其他、grade、desc、status：使用中／已完成、updated）
  - `versions/`：舊版存檔，檔名「原遊戲名稱_YYYYMMDD修改版.html」，同一天第二次為「修改版2.0」
- 更新遊戲：舊的 `index.html` 先複製到 `versions/`，再覆蓋新版。
- 遊戲必須能脫離 Claude 執行（紀錄存在瀏覽器，不使用 Claude 資料庫）。
- 新增資料夾時一併更新 `games/list.json`（首頁的備用清單）。
- 公開網站：檔名與畫面不放學生全名。
