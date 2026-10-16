# AI 體感手搖飲店（GitHub Pages 版）

高中社團課用的網頁：學生填點餐表單 → 產生提示詞 → ChatGPT／Gemini 產生店舖設定碼 → 貼回遊戲 → 拿名片在 webcam 前玩。

| 檔案 | 內容 |
|-|-|
| `index.html` | 課堂講義＋點餐表單（提示詞產生器）；可直接列印成學習單 |
| `game.html` | 體感手搖飲遊戲（名片雙黑點追蹤、職等制、按 E 修改店舖） |

兩個檔案都是單一 HTML，不需要安裝任何東西，也不載入外部資源。

---

## 部署到 GitHub Pages（約 5 分鐘）

1. 登入 GitHub，右上角 **＋ → New repository**
   * Repository name：例如 `bubble-tea-shop`
   * 選 **Public**（GitHub Pages 免費版需要公開）
   * 按 **Create repository**
2. 在新專案頁面點 **uploading an existing file**（或 **Add file → Upload files**）
3. 把 `index.html`、`game.html`（以及這份 `README.md`）拖進去，按 **Commit changes**
4. 進入 **Settings → Pages**
   * Source：**Deploy from a branch**
   * Branch：**main**、資料夾 **/ (root)** → **Save**
5. 等 1～2 分鐘，頁面上方會出現網址：
   `https://<你的帳號>.github.io/bubble-tea-shop/`
6. 打開網址確認講義出現；點「🎮 開啟遊戲」，允許鏡頭，確認名片可以被認出來

之後要更新內容，只要在 GitHub 專案裡重新上傳同名檔案即可，網址不變。

---

## 上課前的小提醒

* **鏡頭權限**：GitHub Pages 是 HTTPS 網址，瀏覽器允許一次後會記住（比直接開本機檔案方便）。
* **網址要短**：可以用短網址或 QR code 投影，學生比較好輸入。
* **換班清除**：遊戲的「修改店舖」會把最後一次套用的設定存在該電腦的瀏覽器；講義的表單內容也會暫存。換班前請在遊戲面板按「↩ 還原預設」、在講義按「清除表單」（有還原卡的電腦重開機也會清掉）。
* **學校網路擋 github.io 時**：把這個資料夾複製到隨身碟，直接雙擊 `index.html` 使用。表單與遊戲都能離線運作，只有 ChatGPT／Gemini 需要連網。
* **AI 連不上時**：表單產生提示詞後，展開「AI 連不上的時候（備案）」可直接複製設定碼（顏色、圖示使用預設值）。

---

## 維護說明

* `game.html` 是專案資料夾中 `bubble-tea-shop_v3.html` 的複本；修改遊戲後請重新複製一份再上傳。
* 學生透過表單只會改到 `SHOP_NAME`、`MENU`、`TOPPINGS`、`TOPPING_PRICE`；其他遊戲參數（糖度、冰塊、職等、營業時間）沿用 `game.html` 內的預設值，可直接在檔案的【店舖設定區】調整。
