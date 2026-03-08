# Prompt Playbook

在 AI 輔助開發中，Prompt 品質直接影響產出結果。本專案提供一組結構化的 Prompt 模板，解決「AI 回覆品質不穩定」和「SA 文件撰寫耗時」的問題。

## Prompt 清單

- **[ai-collaboration-protocol.md](./ai-collaboration-protocol.md)** — 全域 AI 協作協議
  定義與 AI 協作的通用規則：溝通語言、計畫流程、修改範圍控制、Debug 模式等。
  適用於日常 AI 輔助開發，也建議搭配以下任何 SA Prompt 一起使用。

- **[sa-system-level.md](./sa-system-level.md)** — 系統級 SA 文件產生器
  分析整個專案 / 系統，產出完整的系統級 SA Document。
  適用於新系統交接、架構文件補齊。

- **[sa-module-level.md](./sa-module-level.md)** — 模組級 SA 文件產生器
  分析單一 Service、API 或 Job，產出精準的模組級 SA Document。
  適用於開發前 SA Review、單一 API / Job 分析。

## 使用方式

### AI 協作協議

將 `ai-collaboration-protocol.md` 的內容設定為你的 AI 工具的 System Prompt 或自訂指令：

- **Gemini CLI / Code Assist**：放入 `~/.gemini/GEMINI.md`
- **ChatGPT**：貼入「自訂指令 (Custom Instructions)」
- **Claude**：貼入「Project Instructions」或對話開頭

### SA 文件產生器

1. 開啟一個新對話
2. 將對應的 Prompt（system-level 或 module-level）**完整貼入作為第一則訊息**
3. 依序提供專案資料夾結構、設定檔、核心程式碼
4. 輸入 **「開始生成」** 觸發文件產出

詳細流程請參閱各 Prompt 檔案中的 `Input Specification` 章節。

## License

MIT © 2025 Jimmy. See [LICENSE](./LICENSE) for details.
