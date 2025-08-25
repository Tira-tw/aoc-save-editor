# AOC Save Editor
[gbatemp](https://gbatemp.net/threads/wip-beta-aoc-zelda-age-of-calamity-save-editor-money-editing-tools-demo.674649/)


Test Version / 測試版說明

Chinese and English instructions, please choose according to your needs. / 中文與英文說明，請依需要選用。

[中文](#中文說明) / [English](#English)
---

## 中文說明

- 目的與狀態
  - 這是一個前端網頁工具，用於讀取並修改遊戲存檔中的金錢欄位 Money。當前測試版僅支援修改 Money，其他欄位暫不開放。
  - Please note: This is a frontend web tool for reading and modifying the Money field in the game save. The current test version only supports editing Money; other fields are not available yet.

- 主要特性
  - 使用自訂按鈕觸發檔案選取，隱藏原生檔案輸入的按鈕文字
  - 多語言支援（中文 / English），切換語言時會更新介面文字
  - Drag-and-drop 上傳支援（如啟用時）
  - 下載修改後的存檔，檔名將在原檔名基礎上加上 _modified，保留原始副檔名
  - 目前只有 Money 一組偏移量可編輯，偏移量為 126388，使用 Little Endian 32-bit 整數

- 安裝與執行
  - 直接在本機開啟 index.html 即可使用
  - 若要在本機伺服器上執行，例如使用 Python：
    - 進入專案資料夾，執行：`python -m http.server 8000`
    - 打開瀏覽器並前往 http://localhost:8000
  - 或使用你偏好的靜態伺服器

- 使用方式（步驟）
  1) 切換語言（中文 / English）若需要
  2) 點擊「選擇檔案」自訂按鈕，選取要修改的存檔
  3) 程式會顯示 Money 的目前值於「Current」
  4) 在 Modify 欄位輸入新數值，或直接留空以保留原值
  5) 點擊「Download Modified Save」下載修改後存檔，檔名會自動改成原名基礎上追加 _modified，副檔名不變

- 貢獻與參與
  - 若你想參與此專案，歡迎 fork 後提交 PR
  - 請在 PR 中說明你修改的內容與測試步驟

- 版權與許可
  - 本專案採用 MIT 許可，詳見 LICENSE

- 取得與聯絡
  - 如有問題，請於 issue 中提出，我會協助解惑

---

## English

- Purpose and Status
  - This is a frontend web tool to read and modify the Money field in the game save. The current test version only supports editing Money; other fields are not available yet.
  - Note: This is a frontend project; no server-side components are required.

- Key Features
  - Custom Browse button to trigger file selection, hiding the native file input text
  - Multi-language support (Chinese / English); UI text updates when switching language
  - Drag-and-drop upload support (if enabled)
  - Download the modified save; the output filename preserves the original extension and adds _modified
  - Currently, only one offset (Money) is editable: 126388, Little Endian 32-bit integer

- Installation & Running
  - Open index.html directly in a browser to use
  - To run locally with a static server (example using Python):
    - From the project folder, run: `python -m http.server 8000`
    - Open http://localhost:8000
  - Or use any static server you prefer

- How to Use
  1) Switch language if desired
  2) Click the custom Browse button to select the save file
  3) The Money current value will be shown in the Current column
  4) Enter a new value in the Modify column, or leave blank to keep current
  5) Click "Download Modified Save" to download the edited save
  6) The downloaded file name will be original base name + _modified, preserving the original extension

- Contributing
  - If you want to participate, please fork and submit a PR
  - Include a brief description of your changes and testing steps in the PR

- License
  - MIT License (see LICENSE)

- Contact
  - If you have questions, please open an issue and I’ll help
