# 🤖 LLM / 大模型学习路径

> 这条路径从 Transformer 基础走到 LLM 应用实践。根据目标选择需要的部分，不必一次学完所有主题。

## 🎯 建议学习顺序

1. **Transformer 原理**（1 周）—— 现代 LLM 全部基于此
2. **比较模型与服务**（按需）—— 用自己的任务测试，而不是只看排行榜
3. **API 使用**（2 天）—— OpenAI / Anthropic SDK
4. **Prompt 工程**（3 天）—— 让模型输出你想要的结果
5. **RAG & Agent**（1 周）—— 让模型"做事"

---

## 📚 顶级资源（精选）

| 资源 | 评级 | 时间 | 适合 |
|------|------|------|------|
| 📖 [Andrej Karpathy：Neural Networks: Zero to Hero](https://github.com/karpathy/zero-to-hero) | 🌟 必读 | ⏱️ 1w+ | 从零实现 GPT |
| 📖 [Sebastian Raschka：Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch) | 🌟 必读 | ⏱️ 1w+ | 系统实现 |
| 📺 [Andrej Karpathy：A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/) | ✅ 推荐 | ⏱️ 1h | 实战经验 |
| 📖 [LLM Bootcamp（The Full Stack）](https://fullstackdeeplearning.com/llm-bootcamp/) | ✅ 推荐 | ⏱️ 1d+ | LLM 全栈 |
| 📖 [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) | ✅ 推荐 | ⏱️ 1d+ | 工具实操 |

## 🌐 模型与服务目录

模型、接口、价格、上下文长度和地区可用性会不断变化，本页不维护“最强模型”或固定版本列表。查找当前产品时优先使用厂商的模型目录和 API 文档：

- [OpenAI 模型文档](https://platform.openai.com/docs/models)
- [Anthropic 模型概览](https://docs.anthropic.com/en/docs/about-claude/models/overview)
- [Google Gemini 模型文档](https://ai.google.dev/gemini-api/docs/models)
- [DeepSeek API 文档](https://api-docs.deepseek.com/)
- [阿里云百炼模型列表](https://help.aliyun.com/zh/model-studio/getting-started/models)
- [Hugging Face Models](https://huggingface.co/models)

比较时至少检查：目标任务效果、延迟、总成本、上下文限制、数据处理条款、地区可用性和失败处理方式。记录测试日期和提示词；不要把单次体验当成通用排名。

## 🛠️ 工具与框架

| 工具 | 用途 |
|------|------|
| LangChain / LlamaIndex | 构建 LLM 应用与检索工作流；先理解基础流程，再决定是否需要框架 |
| 服务商 SDK | 调用对应模型服务；以服务商当前文档为准 |
| Ollama | 在本地运行部分开源模型；先确认模型许可、硬件需求和支持情况 |
| vLLM | 部署和服务化开源模型；适合有推理部署需求的场景 |

---

## 📂 完整资源列表（附录）

### 必读论文

- Attention Is All You Need (2017)
- BERT (2018)
- GPT-3 (2020)
- Scaling Laws (2020)
- InstructGPT / RLHF (2022)
- FlashAttention (2022)
- LLaMA (2023)
- Mixtral / MoE (2023)

### 进阶资源

- Hugging Face Transformers 文档
- PyTorch Lightning
- DeepSpeed（分布式训练）
- Megatron-LM（NVIDIA 大模型训练）
- LoRA / PEFT（参数高效微调）

---

*内容核查：2026-10-12。官方链接可能变化，使用前请确认当前文档。*
