# kuohuanhuan / blog @ GitHub

![GitHub stars](https://img.shields.io/github/stars/kuohuanhuan/blog?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/kuohuanhuan/blog?style=for-the-badge)

這是 khh.log 的 GitHub 儲存庫。（[網站](https://nekohuan.cyou) 構建的一環。）

`nekohuan.cyou` 儲存庫：https://github.com/kuohuanhuan/nekohuan.cyou

## 添加友情連結

你需要準備：

1. 一個 GitHub 帳號。
2. 一個可編輯 JSON 格式檔案的編輯器（i.e. [Notepad++](https://notepad-plus-plus.org), [VS Code](https://code.visualstudio.com/), [Brackets](https://brackets.io) ……）。
3. 自己的網站資料。

### 在開始之前

請先確認自己的網站符合下列規範：

- 支援 HTTPS，且憑證沒有過期。
- 網站名稱和簡介沒有過長。
- 網站 Avatar：
  + 長寬**不超過** 512px。
  + 託管服務（圖床、Git 儲存庫、網站目錄、雲端硬碟等）可靠（SLA > 75%）。
  + 檔案大小 < 2 MiByte。
  + 可正常辨識，不模糊或呈現格狀。（8-bit / Minecraft / pixel 等風格不在此限。）
  + 靜態圖片。MP4 / MKV 等影片格式禁止，動態 GIF / WebP 等請在 PR 中註明。
- 網站備有「友情連結」頁面 / 區塊。若沒有，可置於頁首或頁尾。
- **網站內容全年齡段適宜。**

### 操作

1. 添加本站資訊到「友情連結」列表中：

- 名稱：`Huan's Log` 或 `khh.log`
- 連結：https://nekohuan.cyou
- 簡介：`$ curl -i https://nekohuan.cyou` 或*其它你認為適合描述我 / [本站](https://nekohuan.cyou) 的句子*。
- Avatar（選擇困難症發作。）：
  + WebP (128x128, ~17.7KB): https://nekohuan.cyou/avatar.webp *（推薦，但[不被較舊版 Safari 支援](https://caniuse.com/webp) 。）*
  + AVIF (128x128, ~2.4KB): https://nekohuan.cyou/avatar.avif *（注意：相容性[非常差勁](https://caniuse.com/avif) 。）*
  + JPG (128x128, ~20.1KB): https://nekohuan.cyou/avatar.jpg
  + PNG (144x144, ~12.8KB): https://nekohuan.cyou/apple-touch-icon.png *（注意：經有損壓縮。）*
  + PNG ([Upload.cc](https://upload.cc) 圖床): https://upload.cc/i1/2023/01/30/WP5BQS.png _（注意：[**可能**對中國大陸 IP 並不友好](https://twitter.com/Uploadcc/status/1463519367325356032)。）_
  + HEIC (128x128, ~1.99KB): https://nekohuan.cyou/avatar.heic *（注意：[目前尚未有瀏覽器支援](https://caniuse.com/heif) ，戰未來。）*

2. 在 GitHub 上 Fork 此儲存庫。

3. 修改 `links.json` 並 commit，格式如下：（注意：請勿更動任何無關檔案。）

```json
  {
    "name": "網站名稱",
    "link": "網址",
    "avatar": "圖片",
    "descr": "簡介"
  }
```

_（注意：上一個物件的大括號（`}`）後請添加半形逗號（`,`），但最後一項（你添加的新物件）請勿尾隨逗號。並請確保 JSON 格式**正確**。建議使用 [JSONLint](https://jsonlint.com) 進行確認。）_

4. 發起 Pull Request 並等待 Merge。

*（注意：本站使用 [GitHack CDN](https://raw.githack.com) 取得 JSON 資料，[GitHub Actions CI](https://github.com/kuohuanhuan/blog/actions) 將在每次 commit 後自動更新前端儲存庫的 JSON 連結。）*

_（注意：本站使用 [ImageKit](https://imagekit.io) 自動將圖片調整成適當大小，並轉換為 WebP 格式。你只需要提供**最穩定**且**不常變動**的圖片連結即可。）_

## 變動 / 更新友情連結

如果出於某些原因，你需要撤下自己的友情連結，請[開個 issue](https://github.com/kuohuanhuan/blog/issues/new) ，**不要**發起 Pull Request。

如果要更新友情連結資訊，請發起 Pull Request。

## 如果友情連結被撤下

可能是因為您的網站……

1. 違反了上述規範。
2. 無法瀏覽。
3. 撤下了本站的連結。（包括設定 CSS 樣式為 `display: none;` 或 `visibility: hidden;` 等行為。）

如果要回覆連結，請確認您的網站已回復到正常狀態，並重新發起 Pull Request。

*如果可以，請附上您的連結被撤下的 commit。（例如：[383986b](https://github.com/kuohuanhuan/blog/commit/383986beb39c3a01ffaaa2d3399e3ccbede85d3d)）*
