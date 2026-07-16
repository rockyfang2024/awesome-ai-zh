# 📘 AI 入门 101（零基础）

> 这一章写给**完全没接触过 AI 的人**。建议顺序阅读。

---

## 第一部分：概念理解（先弄懂"是什么"）

### 1. AI / ML / DL / LLM 的关系

```
┌─────────────────────────────────────┐
│  AI（人工智能）                      │
│  └─ ML（机器学习）                   │
│     └─ DL（深度学习）                │
│        └─ LLM（大语言模型）           │
└─────────────────────────────────────┘
```

| 术语 | 一句话 | 例子 |
|------|--------|------|
| **AI** | 让机器表现出"智能"行为 | 任何智能系统 |
| **ML** | 用数据训练模型，让模型学会规律 | 房价预测、垃圾邮件分类 |
| **DL** | 用深度神经网络做 ML | CNN、RNN、Transformer |
| **LLM** | 大规模语言模型（Transformer + 海量数据）| GPT-4、Claude、文心一言 |
| **GenAI** | 生成式 AI（能生成文字/图片/视频）| ChatGPT、Midjourney、Sora |

### 2. 学习路线分支

| 你想做什么 | 推荐起点 |
|------------|----------|
| **理解原理 / 学术研究** | ML → DL → LLM |
| **做应用 / 创业** | Prompt → LLM API → RAG / Agent |
| **做工程落地** | 直接学 LLM + RAG + Agent |
| **数据科学岗位** | ML → 特征工程 → 模型评估 |

### 3. 必备工具 & 环境

#### Python 环境

```bash
# 推荐用 uv 或 conda
pip install numpy pandas scikit-learn torch transformers
```

#### 必备工具

| 工具 | 用途 | 链接 |
|------|------|------|
| **Python** | 主语言 | python.org |
| **Jupyter Notebook** | 交互式学习 | jupyter.org |
| **VSCode / Cursor** | 代码编辑器 | code.visualstudio.com |
| **Git + GitHub** | 代码管理 | github.com |
| **Hugging Face** | 模型 / 数据集 / Demo | huggingface.co |

#### GPU 资源

| 平台 | 适合 |
|------|------|
| **Google Colab**（免费 GPU） | 初学者 |
| **Kaggle Notebooks**（免费 GPU） | 数据科学 |
| **AutoDL / 恒源云**（国内 GPU） | 国内用户 |
| **AWS / GCP / Azure** | 工程项目 |
| **本地显卡（RTX 4090）** | 个人深度玩家 |

### 4. 主流大模型一览（2026 年）

| 模型 | 公司 | 类型 | 特点 |
|------|------|------|------|
| **GPT-4o / o1 / o3** | OpenAI | 闭源 | 综合能力最强 |
| **Claude 3.5 / 3.7** | Anthropic | 闭源 | 长文本 + 代码 + 工具调用强 |
| **Gemini 2.0** | Google | 闭源 | 多模态 + Google 生态 |
| **DeepSeek V3 / R1** | DeepSeek（国内）| 开源 | 价格屠夫，性能接近闭源 |
| **Qwen 2.5** | 阿里（国内）| 开源 | 中文强 |
| **文心一言 4.0** | 百度（国内）| 闭源 | 集成搜索 |
| **通义千问** | 阿里 | 闭源 + 开源 | 多模态 |
| **豆包** | 字节跳动（国内）| 闭源 | 增长快，C 端 |
| **Kimi** | 月之暗面（国内）| 闭源 | 长文本 |
| **Llama 3.1** | Meta | 开源 | 自部署首选 |
| **Mistral / Mixtral** | Mistral AI | 开源 | 欧洲 |
| **GLM-4** | 智谱 AI（国内）| 闭源 + 开源 | 清华系 |

### 5. AI 能做什么 / 不能做什么

#### ✅ AI 擅长的

- 文本生成、翻译、摘要
- 代码生成、补全、调试
- 图像生成、理解、编辑
- 数据分析、模式识别
- 客服、问答、知识检索

#### ❌ AI 不擅长的

- 精确数值计算
- 100% 准确的事实核查（会"幻觉"）
- 真正的创造性思维（更多是组合）
- 实时信息（训练数据有截止日期）
- 复杂多步推理（O1/R1 改善但仍有局限）

---

## 第二部分：术语速查表

### 基础术语

| 术语 | 含义 |
|------|------|
| **模型（Model）** | 一个参数化的函数（如神经网络） |
| **参数（Parameter）** | 模型学到的权重（GPT-4 约 1.8 万亿参数） |
| **Token** | 文本的最小单位（GPT 一个 token ≈ 0.75 个英文单词） |
| **Embedding** | 把文字/图像转成向量表示 |
| **Prompt** | 输入给模型的文本 |
| **Context** | 模型当前能"看到"的所有内容 |
| **Context Window** | 模型最大上下文长度（GPT-4o = 128K） |
| **Temperature** | 控制生成随机性（0=确定，1=发散） |

### 训练相关

| 术语 | 含义 |
|------|------|
| **Pretrain** | 预训练（用海量无标注文本训练） |
| **Fine-tune** | 微调（在预训练模型上用特定数据继续训练） |
| **RLHF** | 人类反馈强化学习（ChatGPT 的关键技术）|
| **DPO** | 直接偏好优化（RLHF 的简化版） |
| **SFT** | 监督微调（Supervised Fine-Tuning）|
| **蒸馏（Distillation）** | 大模型教小模型 |
| **LoRA / QLoRA** | 高效微调技术 |

### 推理相关

| 术语 | 含义 |
|------|------|
| **Inference** | 模型前向计算（生成结果） |
| **Latency** | 推理延迟 |
| **Throughput** | 每秒 token 数 |
| **Streaming** | 流式输出（一个字一个字吐） |
| **Batch** | 一次处理多条请求 |

### 高级概念

| 术语 | 含义 |
|------|------|
| **RAG** | 检索增强生成（先查资料再回答） |
| **Agent** | 能调用工具、自主完成任务的 AI |
| **Function Calling** | 让模型调用外部 API |
| **MCP** | Model Context Protocol（Anthropic 提出的协议） |
| **MoE** | Mixture of Experts（混合专家） |
| **Hallucination** | 模型"一本正经胡说八道" |
| **Prompt Injection** | 提示注入攻击 |
| **Jailbreak** | 越狱（绕过模型安全限制） |

---

## 第三部分：实操入门（4 步走）

### Step 1：注册大模型账号（10 分钟）

- [ChatGPT](https://chat.openai.com/) — OpenAI（需科学上网）
- [Claude](https://claude.ai/) — Anthropic
- [Gemini](https://gemini.google.com/) — Google
- [通义千问](https://tongyi.aliyun.com/) — 阿里（国内）
- [文心一言](https://yiyan.baidu.com/) — 百度（国内）
- [Kimi](https://kimi.moonshot.cn/) — 月之暗面（国内）
- [DeepSeek](https://chat.deepseek.com/) — DeepSeek（国内，免费）

### Step 2：体验 Prompt（30 分钟）

试试这些场景：
1. **写作**：让它写一篇文章 / 邮件 / 翻译
2. **编程**：让它解释代码 / 找 bug / 写代码
3. **分析**：给它一段数据让它分析
4. **角色扮演**：让它扮演面试官 / 老师 / 医生

### Step 3：用 API（1 小时）

```python
import openai

client = openai.OpenAI()
response = client.chat.completions.create(
    model="gpt-4o",
    messages=[{"role": "user", "content": "你好"}]
)
print(response.choices[0].message.content)
```

### Step 4：跑一个开源模型（2 小时）

```bash
# 用 ollama 本地跑 Llama
ollama run llama3.1
```

或用 LM Studio / GPT4All 图形界面。

---

## 第四部分：入门推荐资源（中文优先）

### 📖 科普 / 入门

| 资源 | 评级 | 时间 |
|------|------|------|
| [3Blue1Brown：神经网络可视化](https://www.3blue1brown.com/topics/neural-networks) | 🌟 必读 | ⏱️ 1-2h |
| [李宏毅《机器学习》](https://speech.ee.ntu.edu.tw/~hylee/ml/) | 🌟 必读 | ⏱️ 1d+ |
| [李沐《动手学深度学习》](https://zh.d2l.ai/) | 🌟 必读 | ⏱️ 1d+ |
| [AI for Everyone（吴恩达）](https://www.coursera.org/learn/ai-for-everyone) | ✅ 推荐 | ⏱️ 1d |
| [《这就是 ChatGPT》](https://book.douban.com/subject/36467877/) | 💡 一般 | ⏱️ 1h |

### 🎓 系统性课程

| 课程 | 评级 | 时间 | 平台 |
|------|------|------|------|
| [吴恩达《机器学习》](https://www.coursera.org/learn/machine-learning) | 🌟 必读 | ⏱️ 1d+ | Coursera |
| [吴恩达《深度学习》专项课](https://www.coursera.org/specializations/deep-learning) | 🌟 必读 | ⏱️ 1w+ | Coursera |
| [Fast.ai 课程](https://course.fast.ai/) | ✅ 推荐 | ⏱️ 1w+ | 官方 |
| [CS231n（斯坦福 CV）](http://cs231n.stanford.edu/) | ✅ 推荐 | ⏱️ 1d+ | 斯坦福 |
| [CS224n（斯坦福 NLP）](http://web.stanford.edu/class/cs224n/) | ✅ 推荐 | ⏱️ 1d+ | 斯坦福 |

---

## 第五部分：常见误区

### ❌ 误区 1：AI = ChatGPT

> AI 是整个领域，ChatGPT 只是其中一个产品（对话 LLM）。
> 还有图像（Midjourney）、视频（Sora）、代码（Copilot）、自动驾驶（Tesla）等。

### ❌ 误区 2：模型越大越好

> DeepSeek R1 用 671B 参数 + 强化学习，达到 o1 水平。
> 关键是**架构 + 训练方法**，不是单纯堆参数。

### ❌ 误区 3：AI 会"思考"

> LLM 本质是**预测下一个 token**，不是真正的逻辑推理。
> 它"看起来"在思考是因为训练数据里有大量的人类思考过程。

### ❌ 误区 4：AI 一定会取代程序员

> AI 改变了程序员的工作方式（从写代码到审代码），
> 但**短期内不会完全取代**。懂得用 AI 的程序员会取代不用的。

### ❌ 误区 5：开源模型不如闭源

> 截至 2026 年初，Llama 3.1 / DeepSeek / Qwen 等开源模型已经接近 GPT-4 水平。
> 在特定任务上甚至超过闭源。

---

## 🎯 给不同背景读者的建议

| 你是什么背景 | 推荐路径 |
|--------------|----------|
| **完全没听过 AI** | 1. 用 ChatGPT 1 周 → 2. 看 3Blue1Brown → 3. 学李宏毅 ML |
| **程序员** | 1. 用 GitHub Copilot / Cursor → 2. 写 RAG 应用 → 3. 学 LLM 原理 |
| **算法工程师** | 1. 读《深度学习》花书 → 2. 复现论文 → 3. 研究 LLM 训练 |
| **产品经理 / 业务** | 1. 体验各家 LLM → 2. 学 Prompt 工程 → 3. 思考 AI 应用场景 |
| **数据科学家** | 1. 巩固 ML 基础 → 2. 学 LLM API → 3. 研究多模态 |

---

## 📚 下一步学习

完成本章后，建议顺序：

1. 📘 [入门 101](01-getting-started.md) ← 你在这里
2. 🧠 [深度学习路径](02-deep-learning-path.md) ← 想懂原理的学这
3. 🤖 [LLM 学习路径](03-llm-path.md) ← 想用 LLM 的学这
4. 📊 [ML 学习路径](docs/04-ml-path.md) ← 想打基础的学这

---

> ⚠️ **数据时效性**：AI 行业变化极快（每 3-6 个月一次大迭代），本节基础概念相对稳定（神经网络/Transformer 这些不会变），但具体模型/工具可能过时。

---

*最后更新: 2026-07-16*