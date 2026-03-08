# 🎯 Prompt Playbook

一套經過迭代打磨的 AI Prompt 工具集，專為軟體工程工作流程設計。

## 📂 Prompt 清單

| 檔案                                                           | 用途                 | 說明                                                                     |
| -------------------------------------------------------------- | -------------------- | ------------------------------------------------------------------------ |
| [ai-collaboration-protocol.md](./ai-collaboration-protocol.md) | 全域 AI 協作協議     | 定義與 AI 協作的通用規則：溝通語言、計畫流程、修改範圍控制、Debug 模式等 |
| [sa-system-level.md](./sa-system-level.md)                     | 系統級 SA 文件產生器 | 分析整個專案 / 系統，產出 13 章節的完整 SA Document                      |
| [sa-module-level.md](./sa-module-level.md)                     | 模組級 SA 文件產生器 | 分析單一 Service、API 或 Job，產出精準的模組級 SA Document               |

## 🚀 使用方式

### AI 協作協議

將 `ai-collaboration-protocol.md` 的內容設定為你的 AI 工具的 System Prompt 或自訂指令：

- **Gemini**：放入 `~/.gemini/GEMINI.md`
- **ChatGPT**：貼入「自訂指令 (Custom Instructions)」
- **Claude**：貼入「Project Instructions」或對話開頭

### SA 文件產生器

1. 開啟一個新對話
2. 將對應的 Prompt（system-level 或 module-level）**完整貼入作為第一則訊息**
3. 依序提供專案資料夾結構、設定檔、核心程式碼
4. 輸入 **「開始生成」** 觸發文件產出

詳細流程請參閱各 Prompt 檔案中的 `Input Specification` 章節。

## 📋 適用場景

| 場景                     | 使用哪份 Prompt                |
| ------------------------ | ------------------------------ |
| 新系統交接、架構文件補齊 | `sa-system-level.md`           |
| 開發前 SA Review         | `sa-module-level.md`           |
| 單一 API / Job 分析      | `sa-module-level.md`           |
| 日常 AI 輔助開發         | `ai-collaboration-protocol.md` |

## 📝 License

MIT
