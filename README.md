# 東京家庭旅遊｜五日行程

單一檔案的行程網站（`index.html`），手機優先，無需建置。

## 功能
- 兩種外觀可切換（右上角設定）：冬夜藍（支援深色模式）、手繪繪本（淺色、插圖動畫）
- 每日行程、出發倒數（家人 12/4 與哥哥 12/2 兩種行程切換）
- 旅行中自動跳到當天、旅行結束提示
- 行李清單與行前準備打勾（存在瀏覽器 localStorage）
- 旅行當天標出「下一個」行程
- Visit Japan Web 住宿欄一鍵複製
- 記帳：單筆記日期、項目、金額（日圓或台幣）、備註、照片，可標「要退稅」並篩選；儀表板加總；換算用花錢那天鎖定的匯率（補記會追溯）
- 天氣：每天行程顯示當地天氣，一天自動更新一次，可手動重新整理（日本氣象廳 7 天；更遠用 Open-Meteo，備援 MET Norway）
- 景點 Google 地圖連結；🆘 求助頁（緊急電話、日文句子、當天集合點）；🚕 給司機看的飯店卡

## 發布到 Claude
改完 index.html 後執行 `python _publish/build.py`，再發布 `_publish/東京家族旅行.html`（`_publish/` 只在本機，不放 GitHub）。Claude 的頁面不能連外，匯率要手動輸入、天氣改顯示查詢按鈕。

## 本機預覽
直接用瀏覽器開啟 `index.html`。

## 部署到 GitHub Pages
1. 在 GitHub 建立新 repository
2. 推送本專案
3. Settings → Pages → Branch 選 `main`、資料夾 `/ (root)` → Save
4. 幾分鐘後即可用 `https://<帳號>.github.io/<repo>/` 開啟

## 注意
內含航班與行程資訊。若不想公開，請建立 **Private** repository
（GitHub Pages 對私人 repo 需付費方案），或確認可公開後再上傳。
頁面已設定 `noindex`，但不等於保密。
