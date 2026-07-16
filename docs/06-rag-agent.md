# 🔗 RAG & Agent

> 让 LLM 不只是聊天，而是能**做事**。

## 🎯 核心概念

### RAG（Retrieval-Augmented Generation）

让 LLM 在回答前**先查资料**：
1. 用户问题 → 转 embedding
2. 向量数据库查找相似文档
3. 把相关文档 + 用户问题一起给 LLM
4. LLM 基于文档回答（不靠"记忆"）

### Agent

让 LLM **自主决策 + 调用工具**：
1. 用户给目标
2. LLM 思考："我需要先做 X，再做 Y"
3. 调用工具（搜索、代码、API）
4. 反思结果，调整计划
5. 循环直到完成

---

## 📚 顶级资源（精选）

| 资源 | 评级 | 时间 | 适合 |
|------|------|------|------|
| 📖 [LangChain Documentation](https://python.langchain.com/) | 🌟 必读 | ⏱️ 1d+ | RAG/Agent 框架 |
| 📖 [LlamaIndex Documentation](https://docs.llamaindex.ai/) | 🌟 必读 | ⏱️ 1d+ | RAG 专用 |
| 📺 [DeepLearning.AI: LangChain for LLM Application Development](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) | ✅ 推荐 | ⏱️ 1h | 入门 |
| 📺 [DeepLearning.AI: AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) | ✅ 推荐 | ⏱️ 1h | Agent 实战 |
| 📖 [Anthropic: Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) | 🌟 必读 | ⏱️ 30min | 设计模式 |

## 🛠️ 主流框架

| 框架 | 评级 | 特点 |
|------|------|------|
| **LangChain** | 🌟 必读 | 最流行 |
| **LlamaIndex** | 🌟 必读 | RAG 首选 |
| **LangGraph** | ✅ 推荐 | Agent 工作流 |
| **CrewAI** | ✅ 推荐 | 多 Agent 协作 |
| **AutoGen（Microsoft）** | ✅ 推荐 | 多 Agent |
| **Semantic Kernel** | 💡 一般 | .NET 系 |

## 🗄️ 向量数据库

| 数据库 | 评级 | 特点 |
|------|------|------|
| **Chroma** | ✅ 推荐 | 简单上手 |
| **FAISS（Meta）** | 🌟 必读 | 经典 |
| **Qdrant** | ✅ 推荐 | 高性能 |
| **Milvus** | ✅ 推荐 | 国产老牌 |
| **Weaviate** | ✅ 推荐 | 易用 |
| **pgvector** | ✅ 推荐 | PostgreSQL 扩展 |

---

## 📂 完整资源列表（附录）

### 进阶主题

- 高级 RAG（Hybrid Search / Re-ranking）
- GraphRAG
- Multi-modal RAG
- Agent Memory 系统
- MCP（Model Context Protocol）

### 工具

- [Flowise](https://flowiseai.com/) — 拖拽式 Agent 构建
- [n8n](https://n8n.io/) — 工作流自动化
- [Dify](https://dify.ai/) — 国内 LLM 应用平台
- [Coze](https://www.coze.com/) — 字节 AI Bot 平台

---

*最后更新: 2026-07-16*