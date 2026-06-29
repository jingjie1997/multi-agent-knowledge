# 🧠 多 Agent 系統學習知識庫

> 矽谷工程師視角 — 彙整 Anthropic 工程部落格、實戰心得、學術研究（2025–2026）

---

## 這份知識庫是什麼？

這是一份針對 **多 Agent AI 系統**的中文學習筆記，從矽谷工程師的實戰角度出發，整合了 Anthropic、Google Research、CooperBench 等最新研究成果，並收錄了生產環境中真實踩過的坑與解法。

適合對象：
- 想導入 AI Agent 系統的工程師
- 正在評估多 Agent 架構的技術決策者
- 對 LLM 應用系統設計感興趣的學習者

---

## 目錄

| 章節 | 內容 |
|------|------|
| [為什麼需要多 Agent？](multi-agent-knowledge.md#為什麼需要多-agent) | 核心驅動力、關鍵數據、何時「不該」用 |
| [三大編排模式深度比較](multi-agent-knowledge.md#三大編排模式深度比較) | Subagent、Agent Team、Dynamic Workflow 比較 |
| [選擇決策樹](multi-agent-knowledge.md#選擇決策樹) | 快速判斷該用哪種架構 |
| [矽谷工程師踩過的坑](multi-agent-knowledge.md#矽谷工程師踩過的坑) | 6 大常見失敗模式與解法 |
| [生產環境工程實踐](multi-agent-knowledge.md#生產環境工程實踐) | Prompt、架構、可觀測性、規模化 |
| [現實狀況 & 未來方向](multi-agent-knowledge.md#現實狀況--未來方向) | 業界數據、2026 趨勢、定義爭議 |

---

## 核心重點摘要

### 三大架構模式

| 模式 | 結構 | 最適場景 |
|------|------|---------|
| **Subagent** | Parent 派工 → 子代理並行執行 | 大量同質、邊界清晰的批次任務 |
| **Agent Team** | 不同角色平行協作 | 長期跨職能專案、需要審核機制 |
| **Dynamic Workflow** | 單 Agent 自適應 | 步驟相互依賴、探索性調查 |

### 關鍵數據

- **+90.2%** — Anthropic 多 Agent 研究系統 vs 單 Agent Claude Opus 4
- **−70%** — 強制套用多 Agent 於串行任務的效能退化
- **15×** — 多 Agent 相較於一般對話的 token 用量倍數
- **25%** — 兩個 AI Agent 協作成功率（約為單 Agent 的一半）

### 黃金法則

> 從 **Dynamic Workflow** 開始，有具體理由才升級到 Subagent 或 Agent Team。  
> 不是因為「更多 Agent 感覺更強大」。

---

## 框架選型快速參考

| 框架 | 適合場景 |
|------|---------|
| **LangGraph** | 有狀態的生產工作流 |
| **CrewAI** | 最快從 demo 到可用原型 |
| **AutoGen / AG2** | 對話式 Agent 團隊 |
| **OpenAI Agents SDK** | 第一方簡單編排 |
| **Claude Agent SDK** | Anthropic 生態編排 |

---

## 資料來源

- Anthropic Engineering Blog — *How we built our multi-agent research system*（2025.06）
- MindStudio — *Claude Code Dynamic Workflows vs Agent Teams vs Sub-Agents*（2026.05）
- Google Research — Agent scaling study
- CooperBench — *Why Coding Agents Cannot be Your Teammates Yet*（2026）
- EITT Academy — *AI Agents 2026 Guide*（2026.05）
- Medium / Micheal Lanham — *Multi-Agent in Production in 2026: What Actually Survived*（2026.04）

---

## License

MIT
