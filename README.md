# 感官地圖 · 橫琴—澳門

Hengqin–Macau Sensory Atlas

以建築、道路標誌與日常聲景為切入點，探索橫琴與澳門之間跨越地理邊界的城市感知、文化記憶與生活經驗。

這是可以直接部署至 GitHub Pages 的完整靜態網站，不需要安裝 Node.js 或執行打包指令。

## 使用 GitHub 網頁上傳與公開展示

1. 登入 GitHub，建立一個 **Public** 倉庫，例如 `sensory-atlas`。
2. 使用 **Add file → Upload files**（空倉庫也可選 uploading an existing file），上傳本資料夾內的所有檔案及子資料夾，並提交至 `main` 分支。
3. 確認倉庫首頁直接看得到 `index.html`、`app.js`、`style.css`、`assets/` 和 `vendor/`。`index.html` 應位於倉庫根目錄。
4. 開啟 **Settings → Pages**。
5. 在 **Build and deployment → Source** 選擇 **Deploy from a branch**。
6. 在 **Branch** 選擇 **main**，資料夾選擇 **/ (root)**，點擊 **Save**。
7. 等待發布完成。Pages 頁面會顯示網站連結，通常形式為 `https://你的帳號.github.io/sensory-atlas/`。把這個網址分享給觀眾即可公開展示。

上傳的是 ZIP 解壓後的內容。GitHub 不會把上傳到倉庫的 ZIP 自動解壓成網站。

`.nojekyll` 是隱藏檔；在 macOS Finder 按 `Command + Shift + .` 可以顯示隱藏檔。

## 模型已完整包含

模型下載資源約 55 MB，已切成 5 個分塊，每個最大 12 MiB，適合用 GitHub 網頁上傳。保留 `assets/` 內的全部檔案和原始檔名即可。

第一次開啟時需要等待模型載入。檔案均使用相對路徑，支援 GitHub Pages 的倉庫子路徑。第三方 3D 函式庫已放在 `vendor/`，無需從 CDN 載入；字型使用 Google Fonts，無法連線時會使用系統字型。

## 網站功能

- 全站繁體中文，主標題「感官地圖」。
- 拖曳旋轉、滾輪縮放；手機單指旋轉、雙指縮放。
- 頂部 `space / visual / sound` 切換觀看角度與研究提示。
- 模型上的三個標籤僅展示，不跳轉頁面。
- 「關於計劃」提供完整項目論述。

## 本機預覽

在這個資料夾開啟終端機，執行：

```sh
python3 -m http.server 8000
```

然後在瀏覽器開啟 `http://localhost:8000/`。模型載入需要 HTTP 服務，本機預覽請使用上述方式。

## 修改內容

- `index.html`：主標題、項目介紹與頁面結構。
- `style.css`：排版、顏色與手機樣式。
- `app.js`：標籤位置、觀看角度與互動。
- `assets/`：模型分塊及載入清單。
- `vendor/`：Three.js 與 meshoptimizer。
- `LICENSES/`：第三方函式庫授權。

## GitHub 官方說明

- [設定 GitHub Pages 發布來源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [上傳檔案至 GitHub 倉庫](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
