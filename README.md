# 🚀 Mission Control Center (MCC) - Remix 專案
這是一個基於 Remix.run 框架開發的次世代火箭發射控制台介面。本專案模擬了航太發射中心的即時監控系統，整合了遙測數據視覺化、倒數計時序列以及系統狀態檢核功能。

## 📡 核心功能 (Features)
T-Minus 實時倒數計時：精確至毫秒的發射時序管理系統。
動態遙測面板 (Telemetry)：利用 SSR 與 Client-side 平滑過渡，呈現速度、高度、燃料壓力等模擬數據。
系統狀態檢核表 (Pre-flight Checklist)：基於 Remix Action 的狀態更新系統，模擬發射前的各項硬體確認。
全域警報系統：當偵測到異常數據時，介面會自動切換至 🔴 ABORT 模式並觸發視覺警報。
響應式指揮艙佈局：針對多螢幕環境優化的 Bento Grid 設計。

## 🛠️ 技術棧 (Tech Stack)
框架: Remix (Full-stack Web Framework)
樣式: Tailwind CSS (內含 CSS Grid 佈局)
動畫: Framer Motion (用於數據跳動與面板過場)
圖表: Recharts (歷史遙測曲線繪製)
圖標: Lucide React (航太工業風格圖示)

## 🚀 快速開始 (Quick Start)
1. 複製專案
```bash
git clone github.com
cd rocket-control-center
```

2. 安裝依賴
```bash
npm install
```

3. 啟動開發伺服器
```bash
npm run dev
```

瀏覽器訪問 http://localhost:3000 即可進入指揮介面。
📁 目錄結構
```text
app/
├── components/          # 所有的控制台組件 (Clock, Gauge, Log...)
├── routes/              # 頁面路由 (_index 為主主控制台)
├── styles/              # 全域樣式與 Tailwind 配置
├── hooks/               # 自定義 React Hooks (如 useCountdown)
└── utils/               # 物理公式計算與數據模擬邏輯
```

## ⚠️ 異常中止協議 (Abort Protocol)
若在開發過程中遇到嚴重 Bug，請執行：
按下介面上的紅色 ABORT 按鈕。
檢查伺服器端日誌（Server Logs）。
修復 app/routes/ 下的邏輯錯誤後重新啟動。

## 👨‍🚀 開發者備註
本計畫旨在透過 Remix 的強大效能模擬極端環境下的數據交換。如果你對航太設計或 UI/UX 有更好的建議，歡迎提交 Pull Request。
"Ad Astra per Aspera" (循此苦旅，以達天際)

## 💡 建議接下來的操作：
建立組件庫：先從最簡單的 Countdown.tsx 開始寫起。
視覺風格：在 tailwind.config.js 中定義一組專屬於控制台的顏色（如 terminal-green: #00FF41）。
數據模擬：寫一個 setInterval 來模擬高度與速度的遞增。



