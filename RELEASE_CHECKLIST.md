# CLX／CLZ 發布作業檢查表

> 此檔案用於避免「本機修改完成、卻沒有同步 GitHub／Vercel」的重複失誤。每次修改都必須依順序執行，完成前不得向使用者宣稱已上線。

## 專案位置與必要資訊

- GitHub Repository: `bomber79225/clx-clz-visualizer`
- Branch: `main`
- 線上實際入口: https://clx-clz-visualizer-bomb8.vercel.app/
- Vercel Team: `team_AAcrOxu9PGpGyQI6hpiccMNG`
- Vercel Project: `prj_BMRgYiQXyZvuqDpj2Qe8xwOvnnr7`
- GitHub 程式目前部署形式: 完整單頁 `index.html`（包含樣式、程式和內嵌費率）。
- **重要:** 現有 Vercel 專案採 API 直接部署，GitHub 與 Vercel 尚未設定自動 Git push 部署。每次修改都必須**另外部署 Vercel**；不能只更新 GitHub。

## 嚴格發布流程

1. **先確認工具是否可用**：檢查 GitHub 的 `fetch_file`/`update_file`，Vercel 的 `get_project`/`create_deployment`/`web_fetch_vercel_url`。不得未查驗就聲稱沒有權限或工具不可用。
2. **檢查現有程式版本**：讀取 GitHub 的 `main:index.html` 和原始檔。確認最新使用者要求，保留費率及各項給付的檢核。
3. **修改、測試與產出部署版**：檢查手機排版、字型溢出風險、文案儲存、變數插入、保額切換、複製圖片及文字。測試不到的功能要明說。
4. **先更新 GitHub**：讀取最新檔案 SHA，提交完整修改後的 `index.html` 到 `main`；保留 commit SHA。若寫入失敗，不得宣稱同步成功。
5. **再發布 Vercel**：對上述既有 project 做 production deployment，確保回報 `READY` 且 alias 指向正式網址。
6. **驗證網站實際內容**：重新讀取 `https://clx-clz-visualizer-bomb8.vercel.app/`，必須取得 HTTP 200；比對線上 HTML 與 GitHub `main:index.html` **完全一致**，並查驗本次修改標記（標題、字級、動態欄位、儲存邏輯等）。
7. **最後才能通知使用者**：簡述已更新的內容，附上正式網站網址、GitHub 連結與 commit SHA。若某一步失敗，應指出失敗步驟和現有狀態，切勿說「已上線」。

## 變更安全原則

- 原始 `haahabcalculater` 不修改；僅對 CLX／CLZ 專案作業。
- 年繳費率以建議書中的實際費率表為準；超出可規劃年齡、保額範圍時禁止報價／複製。
- 客戶文案儲存在**本機瀏覽器 localStorage**，非跨裝置同步；須向使用者清楚說明。
- 圖卡文案要保留給付條件、等待期及不保證理賠等必要說明。
- 若要真正實現 GitHub 每次 push 自動部署，須另行在既有 Vercel 專案建立 Git Integration，不能把目前的「每次 API 直接部署」說成自動同步。

## 最後成功驗證

- 2026-11-11：GitHub commit `c7643298a8fce4cb3bca566ed9524e22b5042baf`
- Vercel Production deployment `dpl_J4jdXQsJssEWB8YhPWQ14ax5Y1Pm`
- 線上 HTTP 200；線上 HTML 與 GitHub `main:index.html` 完全一致。
- 驗證的變更：標題為「一張圖，看懂這份防癌保障」；客戶資訊顯示「100萬元保額」；主要數字字級 152px、次保障字級 46px（桌面版），保留 localStorage 儲存機制。
