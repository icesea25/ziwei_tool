# 紫微排盤工具

三合派紫微斗數排盤網頁工具，精簡星曜、支援真太陽時校正、大限／流年互動查詢。純前端、單一 HTML 檔，沒有後端、不會把任何資料送出去。

## 放到 GitHub Pages 上線

1. 在 GitHub 建一個新的 repository（public 或 private 都可以，private 的話 Pages 要付費方案才能開）。
2. 把這個資料夾裡的 `index.html` 上傳到 repository 的根目錄（檔名一定要是 `index.html`，GitHub Pages 才會自動當首頁）。
3. 到 repository 的 **Settings → Pages**，「Source」選 `Deploy from a branch`，Branch 選 `main`（或你的預設分支）／`/ (root)`，存檔。
4. 等 1 分鐘左右，GitHub 會給你一個網址，格式大概是：
   `https://<你的帳號>.github.io/<repository名稱>/`
5. 打開這個網址就能直接用了，之後每次改 `index.html` 重新 push，網站會自動更新。

也可以不用 GitHub Pages，直接把 `index.html` 下載到手機或電腦，雙擊用瀏覽器打開一樣能用（存檔功能一樣有效，只是資料只留在那台裝置、那個瀏覽器裡）。

## 資料存在哪裡

「存入命盤庫」的命盤資料存在瀏覽器的 `localStorage` 裡，只留在**這台裝置、這個瀏覽器**上，不會同步到別的裝置，也不會被上傳到任何伺服器。清瀏覽器資料或用無痕模式會讓存檔消失。

## 與 Claude 版本的差異

這個 `index.html` 和你在 Claude 對話裡用的 artifact 版本是**同一份程式碼**，會自動偵測環境：在 Claude 裡執行時優先用 Claude 提供的雲端儲存（可以跨裝置、跨對話保留），在一般瀏覽器（例如 GitHub Pages）執行時自動改用 `localStorage`。所以同一個檔案兩邊都能用，不需要維護兩份程式碼。

## 瀏覽器建議

排盤需要用到瀏覽器內建的中國農曆換算功能（`Intl` 的 `chinese` 曆法），建議用 **Chrome、Edge，或其他 Chromium 系瀏覽器**，相容性最好。部分較舊版本的 Safari／Firefox 可能不支援，農曆換算會出錯。

「截圖」功能需要從網路載入一個小套件（html2canvas）才能運作，第一次使用時電腦或手機要能連上網路；離線環境下這個按鈕會顯示提示，其餘排盤功能不受影響。

## 免責聲明

紫微斗數為傳統命理參考工具，排盤結果僅供自我認識與思考之用，非科學論斷。
