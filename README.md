# tradingview-widgets

## ✨ 功能 (Features)

*   **全螢幕佈局**: 自動填滿整個瀏覽器視窗，提供沉浸式的分析體驗。
*   **響應式網格**: 使用 CSS Grid 建立的 2x2 佈局，在不同螢幕尺寸上都能保持美觀。
*   **多圖表顯示**: 預設顯示 ETH, SOL, ADA, SUI 四種加密貨幣對 USDT 的圖表。
*   **獨立圖表面板**: 每個圖表都有自己的標題列，介面清晰，易於辨識。
*   **預載技術指標**:
    *   **Williams Alligator (鱷魚線)**: 用於判斷市場趨勢和盤整（糾結）狀態。
    *   **MACD**: 用於輔助判斷趨勢動能和潛在的交叉訊號。
*   **高度可攜性**: 整個應用程式只包含一個 `index.html` 檔案，無需伺服器、無需安裝、無需編譯。
*   **乾淨的深色主題**: 儀表板整體採用深色主題，圖表則為白色背景，適合長時間觀看。


#### 修改技術指標 (Indicators)

在 `createTradingViewWidget` 函數中找到 `studies` 陣列：
```javascript
"studies": [
    {
        "id": "WilliamsAlligator@tv-basicstudies",
        "styles": { /* ... */ }
    },
    {
        "id": "MACD@tv-basicstudies"
    }
],
```
*   **移除指標**: 直接刪除您不想要的指標物件即可。
*   **新增指標**: 新增一行指標 ID，例如要加入 RSI：
    ```javascript
    "studies": [
        "WilliamsAlligator@tv-basicstudies",
        "MACD@tv-basicstudies",
        "RSI@tv-basicstudies" // 新增 RSI
    ],
    ```

[Advanced Real-Time Chart Widget](https://www.tradingview.com/widget-docs/widgets/charts/advanced-chart/)  
[settings.html](https://github.com/karanlyons/binance-enhanced/blob/master/settings.html)