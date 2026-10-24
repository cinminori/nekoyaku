0.1.8：舊版 WebView 也能正常顯示 KakaoPage。

有些裝置出廠的系統 WebView 很舊（例如 Supernote Nomad 是 Chrome 96），又沒辦法更新。KakaoPage 的網站用了新的 CSS 語法（`@layer`），舊 WebView 看不懂會把整份樣式丟掉，頁面變成一堆藍色連結的純文字排版。這版在 WebView 版本太舊時，App 會自己把網站的 CSS 整理成舊版看得懂的寫法再交給它，版面就正常了。新機器不受影響。

- 判斷方式：WebView 是 Chrome 99 以前才啟用，其他裝置完全走原本的路
- 舊 WebView 本來就不支援的細節（`:has()`、容器查詢、`color-mix()`）還是會略過，個別元件可能跟新機器略有差異
- 從 0.1.5 以上更新直接覆蓋安裝即可，設定與譯文都會保留

---

NekoYaku 功能一覽：

- 內建瀏覽器＋「翻譯這裡」邊捲邊翻（韓漫旁註、日漫對話框蓋字）
- 作品名詞表、前情摘要、每話譯文存檔
- 文A 網頁介面翻譯（Google）
- BookWalker 直向捲動與翻頁模式
- 電子紙模式

支援 Android 7.0+、arm64。安裝後到設定填 Gemini API Key 即可使用。
