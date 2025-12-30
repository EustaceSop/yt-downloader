# 🎬 1337 Downloader - YouTube Video Converter

一個基於 HTML/JS 的輕量化 YouTube 影片轉換工具。透過整合第三方 API，提供便捷的 MP3 與 MP4 格式轉換服務。

## ⚠️ 重要運行說明

**本專案無法直接點擊 `index.html` 檔案運行。** 由於瀏覽器的安全性政策 (Same-Origin Policy)，`iframe-resizer` 指令與外部 API 必須在 **Web Server 環境** 下運作。

- **推薦部署方式**：使用 GitHub Pages、Vercel、Netlify 或本地環境的 Live Server (VS Code Extension)。
- **環境要求**：必須透過 `http://` 或 `https://` 協議訪問。

## ✨ 功能特色

- **免安裝服務**：完全基於瀏覽器運作，無需下載任何執行檔或插件。
- **雙格式支援**：支援轉換為高品質 MP3 或 MP4 格式。
- **智能主題切換**：可選擇「淺色」、「深色」或「跟隨系統預設」主題介面。
- **自動適應介面**：使用 `iframe-resizer` 技術，確保轉換器內容在不同裝置上都能完美顯示。
- **短連結相容**：同時支援標準 YouTube 網址 (`youtube.com`) 與短網址 (`youtu.be`)。
- **法律合規聲明**：內建完整的法律提示與使用規範，確保用戶了解版權責任。
- **安全沙箱控制**：針對 API 內容設定 `sandbox` 權限，確保主站安全性。

## 🚫 已知限制

- **不支援 YouTube Shorts**：目前無法解析短影音連結 (`youtube.com/shorts/`)。
- **解析範圍**：僅支援標準影片網址 (`youtube.com/watch?v=...`)。
- **區域限制**：部分受版權保護或地區限制的影片可能無法成功轉換。

## 🚀 部署指南

### 使用 GitHub Pages (免費推薦)
1. 將 `index.html` 上傳至 GitHub 倉庫。
2. 進入倉庫的 **Settings** > **Pages**。
3. 在 Build and deployment 區塊將 Source 設定為 **Deploy from a branch**。
4. 選擇 `main` 分支並儲存，稍等幾分鐘後即可透過專屬網址使用。

### 使用本地開發環境
如果您要在本地端進行測試，請使用：
- **VS Code**: 安裝 `Live Server` 擴充功能並右鍵點擊 "Open with Live Server"。
- **Python**: 在資料夾下執行 `python -m http.server 8000`。

## 🛠 技術棧

- **Frontend**: HTML5, CSS3, JavaScript (ES6+).
- **Libraries**: [iframe-resizer](https://github.com/davidjbradshaw/iframe-resizer) (確保 API 內容高度動態調整)。
- **Backend API**: 整合 `clickapi.net` 的 WidgetPlus 轉換介面。

## ⚙️ 開發細節

- **URL 驗證**：前端腳本會自動檢查輸入網址的合法性，防止無效請求。
- **非同步載入**：採用延遲載入機制確保 iframe 重置，優化使用者體驗。
- **安全沙箱**：iframe 設定了嚴格的 `sandbox` 屬性，在允許下載與腳本運行的同時，最大程度保障主頁面的安全。

## ⚠️ 法律與免責聲明

本工具僅供個人學習與學術研究使用。使用者在下載內容前，應確保已獲得版權所有者的許可，或該內容屬於公有領域/標註有 Creative Commons 授權。
**本專案不對使用者下載的任何非法內容負責。**
`文檔由Gemini協助撰寫(因為有些markdown格式我不會), 網頁內容由ChatGPT提供協助, 詳細技術及利用原理由Discord用戶"whitehexrust"提供`

## 📜 許可證
本專案基於 MIT 許可證開源。
