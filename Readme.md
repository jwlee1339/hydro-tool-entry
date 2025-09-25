# 水文工具入口網站 (Hydro Tools Entry Page)

這是一個使用 HTML, CSS 和 JavaScript 建立的靜態首頁，作為所有水文相關工具網站的統一入口。頁面採用了 Bootstrap 5 框架，實現了現代化且響應式的設計。

**線上展示:** [點擊查看](https://jwlee1339.github.io/Hydro/01_HydroEntry/)

---

## ✨ 功能特色

- **動態工具卡片**: 所有工具連結皆由 `index.html` 內的 JavaScript 動態生成。未來若需新增、修改或刪除工具，僅需維護 `tools` 陣列資料，無需更動 HTML 主體結構。
- **響應式設計**: 使用 Bootstrap 5 的網格系統，頁面在桌面、平板和手機等不同尺寸的裝置上都能完美顯示。
- **深色/淺色模式**:
  - 右下角提供模式切換按鈕，可在淺色與深色主題間自由切換。
  - 網站會記住您的選擇 (`localStorage`)，下次訪問時將自動套用您偏好的主題。
  - 若無儲存的偏好，則會根據您作業系統的設定自動選擇初始主題。
- **回到頂部按鈕**: 當頁面向下滾動時，左下角會出現「回到頂部」按鈕，點擊後可平滑滾動至頁面頂端。
- **互動式動畫**:
  - 當滑鼠懸停在工具卡片上時，卡片會輕微放大。
  - 同時，卡片上的圖示會產生生動的搖擺動畫，提升使用者互動體驗。

## 🛠️ 技術棧

- **HTML5**
- **CSS3**: 包含 `@keyframes` 動畫。
- **JavaScript (ES6+)**:
  - 使用 `DOMContentLoaded` 確保頁面元素加載完畢後才執行腳本。
  - 使用 `map()` 和 `join()` 高效生成 HTML 內容。
  - 使用 `MutationObserver` 監聽主題變化，實現穩定的 UI 更新。
- **Bootstrap 5**: 用於版面配置、卡片元件和顏色模式。
- **Bootstrap Icons**: 提供頁面中所有的向量圖示。

## 🚀 如何更新

若要新增或修改工具連結，請開啟 `index.html` 檔案，並找到 `<script>` 區塊中的 `tools` 陣列。

```javascript
// --- Card and Footer Logic ---
const tools = [
    {
        name: "新的工具名稱",
        icon: "bi-star-fill", // 從 Bootstrap Icons 選擇一個圖示
        url: "https://example.com",
        description: "這個新工具的簡短描述。"
    },
    // ... 其他工具
];
```

只需依照上述格式修改此陣列，頁面內容便會自動更新。
