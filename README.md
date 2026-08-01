# Cocogo

雙語對照閱讀。原文一行、譯文一行，陪你把整本原文書讀完。

支援網頁翻譯、選字翻譯與影片字幕，可自行接上 OpenAI、Claude、Gemini、DeepL 等翻譯服務。

---

## 這個儲存庫是什麼

這裡存放 Cocogo 的**公開資源**，由擴充功能在執行期取用：

| 檔案 | 用途 |
| --- | --- |
| `cocogo-rules_v2.json` | 網站適配規則（穩定版） |
| `cocogo-rules-on_v2.json` | 網站適配規則（預設開啟翻譯） |
| `cocogo-rules-off_v2.json` | 網站適配規則（預設關閉翻譯） |
| `version.txt` | 版本檢查用的版本號 |
| `README*.md` | 擴充功能「關於」頁顯示的內容 |

---

## 網站適配規則

不同網站的排版差異很大，適配規則負責告訴 Cocogo：這個網站的**內文段落**是哪些元素、哪些區塊（選單、按鈕、程式碼）**不要翻譯**。

規則透過訂閱機制更新，不需要重新安裝擴充功能。

### 回報規則問題

某個網站翻譯錯位、漏翻，或是把選單也翻了？歡迎[開一個 issue](https://github.com/gaopei0924/cocogo-rules/issues/new)，請附上網址與畫面截圖。

### 安全說明

Cocogo 在載入遠端訂閱規則時，會**一律剝除規則中的可執行腳本欄位**（`injectJs`、`transStartHook`、`transEndHook`）。

這代表：即使規則來源被入侵，也無法透過規則在你造訪的網頁上執行任何程式碼。只有你自己在本機手動輸入的規則才能攜帶腳本。

---

## 授權 / License

### Cocogo 擴充功能本體

Cocogo 以 **GNU General Public License v3.0（GPL-3.0-only）** 授權。

Cocogo 是衍生作品，改作自 **[KISS Translator](https://github.com/fishjar/kiss-translator)**，原作者 **Gabe**，同樣以 GPL-3.0 授權。原著作權聲明依 GPL-3.0 第 4 條完整保留於本專案的 `LICENSE` 與 `NOTICE` 檔案中。

依 GPL-3.0 第 6 條，取得 Cocogo 的使用者有權取得完整對應原始碼。

> **原始碼取得方式**：Cocogo 的程式碼儲存庫目前為私人儲存庫，將於首次公開發行前轉為公開。在此之前如需取得原始碼，請透過本儲存庫的 issue 聯繫。

### 網站適配規則

本儲存庫中的 `cocogo-rules*.json` 改作自 **[kiss-rules](https://github.com/fishjar/kiss-rules)**（作者 Gabe），原專案以 **MIT License** 授權，特此致謝。

### 無擔保聲明

本程式係基於「現狀」提供，不附任何形式之擔保，包括但不限於適售性及特定目的適用性之擔保。使用本程式所生之風險由使用者自行承擔。詳見 GPL-3.0 第 15 條與第 16 條。
