# Zero to Master：前端

從零到 L3 軟體工程師的前端學習路線，by [MirrorStack](https://mirrorstack.com)。

## 核心概念

你是**駕駛**，AI 是**副駕**。你要學的是怎麼叫 Claude Code 幫你寫出正式上線的軟體 — 寫規格、看 code、交出乾淨的 PR。不用背語法，重點是看得懂、能判斷、會下指令。

## 等級

| 等級 | 職稱 | 能幹嘛 |
|------|------|--------|
| L3 | 軟體工程師 | 寫規格、指揮 Claude、看 code review、交付有測試跟 Story 的元件 |
| L4 | 資深工程師 | 自己扛功能、做架構決定、帶 L3、做沈浸式體驗 |

## 學習路線

### Phase 00 — 環境設定（Day 0）

> 把所有開發工具裝好。

[00-環境設定.md](00-環境設定.md)

---

### Phase 01 — 終端機跟 Git（Day 1）

> 學會操作檔案、開分支、用 GitHub。

[01-終端機與Git.md](01-終端機與Git.md)

---

### Phase 02 — Claude Code：入門（Day 1-2）

> 打開 Claude、問問題、用對話搞懂程式碼在幹嘛。

[02-Claude-Code-基礎.md](02-Claude-Code-基礎.md)

---

### Phase 03 — Claude Code：規格驅動開發（Day 2-3）

> 用白話寫規格，Claude 來寫 code，你來看對不對。

[03-Claude-Code-規格驅動開發.md](03-Claude-Code-規格驅動開發.md)

---

### Phase 04 — Claude Code：團隊流程（Day 3）

> start-issue、叫 Claude 寫、/simplify、/commit、開 PR。

[04-Claude-Code-團隊工作流程.md](04-Claude-Code-團隊工作流程.md)

---

### Phase 05 — 看 Code 跟 Review（Day 4-5）

> 看 HTML、CSS、TypeScript、React、Tailwind — 看懂 Claude 寫出來的東西、抓 bug。

[05-閱讀與審查.md](05-閱讀與審查.md)

---

### Phase 06 — 用測試當規格（Day 6）

> 用中文寫「這個元件應該要怎樣」，Claude 幫你轉成 Vitest 測試。AI 版的 TDD。

[06-測試即規格.md](06-測試即規格.md)

---

### Phase 07 — Storybook（Day 7）

> 把元件用視覺的方式記錄下來。寫 Story、設 Controls、在瀏覽器裡看效果。

[07-Storybook.md](07-Storybook.md)

---

### Phase 08 — 第一個元件（Day 8-10）

> 有人帶著做：寫規格 → Claude 實作 → 測試 → Story → 開 PR。你第一次對真正的 codebase 貢獻。

[08-第一個元件.md](08-第一個元件.md)

---

### Phase 09 — L3 畢業（Day 11-14）

> 自己獨立交付 2-3 個 web-ui-kit 元件。自己回覆 code review。

[09-L3畢業.md](09-L3畢業.md)

---

### Phase 10 — L4 之路（L3 之後）

> Three.js、React Three Fiber、沈浸式網頁、UI/UX、體驗式設計。

[10-L4之路.md](10-L4之路.md)

---

## 怎麼跑

1. 照順序一個一個做
2. 每個 Phase 都接著前一個 — 全部都在真的 codebase 裡面做
3. 你的主要產出是**規格跟 review**，不是 code
4. Claude 寫 code；你負責指揮、看、交付
5. Phase 09 就是 L3 畢業 — 真正 merge 進 `web-ui-kit` 的 PR

## 時程

| Phase | 主題 | 天 |
|-------|------|----|
| 00 | 環境設定 | 0 |
| 01 | 終端機跟 Git | 1 |
| 02 | Claude Code：入門 | 1-2 |
| 03 | Claude Code：規格驅動 | 2-3 |
| 04 | Claude Code：團隊流程 | 3 |
| 05 | 看 Code 跟 Review | 4-5 |
| 06 | 用測試當規格 | 6 |
| 07 | Storybook | 7 |
| 08 | 第一個元件（有帶） | 8-10 |
| 09 | L3 畢業 | 11-14 |
| 10 | L4 之路 | 持續 |

## 授權

MIT
