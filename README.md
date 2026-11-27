# 虎尾國小學習教室

學生遊戲大廳。首頁會自動列出 `games/` 裡的每個遊戲資料夾。

## 上架規則
- 每個遊戲一個資料夾：`games/<英文名稱>/`
  - `index.html`：最新版遊戲（固定檔名，網址才不會變）
  - `info.json`：首頁卡片資料（name、subject：國語／數學／特需／個別化／其他、grade、desc、status：使用中／已完成、updated）
  - 國語課本教材包另加 `publisher`（南一／康軒／翰林）、`semester`（上／下）、`lesson`（課次數字），首頁會依「版本 → 年級學期 → 課次」分組排序；沒有 `publisher` 的遊戲依科目分組
  - `versions/`：舊版存檔，檔名「原遊戲名稱_YYYYMMDD修改版.html」，同一天第二次為「修改版2.0」
- 更新遊戲：舊的 `index.html` 先複製到 `versions/`，再覆蓋新版。
- 遊戲必須能脫離 Claude 執行（紀錄存在瀏覽器，不使用 Claude 資料庫）。
- 新增資料夾時一併更新 `games/list.json`（首頁的備用清單）。
- 公開網站：檔名與畫面不放學生全名。
- 數學遊戲入口頁：首頁的「數學」卡片會先開 `entry.html?g=<資料夾名稱>`，頁面有開始遊戲鍵、學習單（讀 `info.json` 的 `worksheets`）與 QR code（指向 `games/<資料夾名稱>/`，平板掃了直接進遊戲）。遊戲本體仍是各資料夾的 `index.html`，上架流程不變。
- 「特需」分類放主題教材：一個主題一個資料夾，`index.html` 是分頁頁面，各教材另存成同資料夾裡的 html。
