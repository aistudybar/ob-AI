
---
目录：
上一页：
下一页：
关键词：
相关链接：

---

> AI 全栈技术树（AI Full-Stack Tech Tree），覆盖从底层算力 → 模型 → 能力 → 应用 → 安全 → 工程化 → 企业化等。包含常见的AI概念、术语、工具、平台，尤其关注当前求职市场的稀缺职位（如AI工程师）、赚钱副业，如AIGC、知识库、AI编程、自动化工作流、网站内容抓取、博客文章生成、视频创作、视频简报、K12辅助教育等


## 一、底层算力层（Compute & Infrastructure）

### 1. 硬件算力
- **CPU**：x86（Intel / AMD）、ARM（Apple Silicon、Ampere）
- **==GPU==**：NVIDIA（A100 / H100 / L40）、AMD MI 系列，家庭用RTX5090/4090/3090
- **AI 加速器**：
  - TPU（神經處理器 ，Google）
  - NPU（張量處理器，华为 Ascend、Apple Neural Engine）
  - LPU（語言處理器，Groq 这种专为速度而生的 LPU）
  - ？？？FPGA（Xilinx）
  - 国产芯片 (华为昇腾等)
- ？？？**边缘设备**：Jetson、RK、树莓派 + AI 模块

### 2. 算力形态
- 本地算力（Local AI / On-device AI）
- 私有云 / 混合云
- 公有云 GPU
- Serverless AI（按调用计费）

### 3. 云平台：不想自己买显卡就租它们的！
- **国际**：AWS、GCP、Azure、OCI
- **国内**：阿里云、腾讯云、华为云、火山引擎
- **AI 专用云**：
  - AWS Bedrock
  - Azure OpenAI
  - Google Vertex AI
  - ==Hugging Face== (AI界的GitHub)
  - ModelScope (魔搭社区)


---

## 二、系统与基础软件层（System & Foundation）

### 1. 操作系统
- Linux（Ubuntu / CentOS / Rocky）
- 容器 OS（COS、Bottlerocket）

### 2. 容器与调度
- Docker
- Kubernetes（K8s）
- Helm
- KubeFlow

### 3. 加速与并行
- CUDA / ROCm
- ！！！PyTorch （**炼丹炉框架**）大家基本都在用 PyTorch，Google 家的 TensorFlow 和 JAX 也有人用
- NCCL
- DeepSpeed
- Ray


---

## 三、模型层（Model Layer）

### 1. 模型类型
- **基础模型（Foundation Models）**
  - LLM（大语言模型）
  - VLM（视觉语言模型）
  - Diffusion（扩散模型）
  - Multimodal（多模态）

### 2. 主流模型家族
闭源三巨头: GPT-4, Gemini, Claude 3

- **通用大模型**
  - GPT-4 / GPT-4o / GPT-5（OpenAI）
  - Claude（Anthropic）Claude 3.5（写代码超强）
  - Gemini（Google）
  - LLaMA（Meta）
- **中文模型**
  - 通义千问
  - 文心一言
  - 智谱 GLM
  - 百川
- **开源模型**
  - LLaMA（Meta）
  - Mistral
  - DeepSeek
  - Qwen
  - Yi
- **多模态模型**
  - 画图: Midjourney, SDXL, Flux
  - 做视频: Sora, Runway, Kling (可灵)
  - 听与说: Whisper, XTTS
AIGI
画图: Midjourney 审美无敌，Stable Diffusion (WebUI/ComfyUI) 玩法最多。
视频: Runway Gen-3，还有快手的可灵 (Kling)，让照片动起来只需一瞬间。
说话: Whisper 听写超准，ChatTTS 说话跟真人似的。

### 3. 模型能力维度
- 文本生成
- 代码生成
- 图像生成（SD / DALL·E / Midjourney）
- 视频生成（Sora / Pika / Runway）
- 音频生成（TTS / Music）

---

## 四、模型训练与微调（Training & Tuning）

### 1. 训练方式
- 预训练（Pre-training）
- SFT（指令微调，老师傅带徒弟）
- RLHF / RLAIF(按人类喜好调整)
- PEFT (！！！省钱微调法 ==LoRA==)

### 2. 轻量化微调
- LoRA / QLoRA
- Adapter
- Prompt Tuning

### 3. 模型压缩
- Quantization（INT8 / INT4）
- Pruning
- Distillation

---

## 五、AI 核心能力层（AI Capabilities）

### 1. 自然语言能力
- NLU / NLG
- 文本总结
- 翻译 / 改写
- 语义搜索

### 2. 知识与推理
- Chain of Thought
- Tree of Thought
- Tool Calling
- Function Calling

### 3. 多模态能力
- OCR
- 图像理解
- 视频理解
- 语音识别（ASR）

---

## 六、AIGC 能力层（重点）

### 1. 文本 AIGC
- 博客文章生成
- SEO 内容生成
- 新闻摘要
- 社交媒体文案

### 2. 图像 AIGC
- 文生图 / 图生图
- 海报 / 封面 / 插画
- 教育插图

### 3. 视频 AIGC
- 文生视频
- PPT → 视频
- 视频简报（Video Briefing）
- 虚拟主播 / AI 数字人

### 4. 音频 AIGC
- TTS（多语言、多音色）
- 配音 / 播客
- 教学讲解音频

---

## 七、知识库与 RAG（重点）

**进阶**: 加上知识图谱 (GraphRAG)，逻辑更严密。

### 1. 知识来源
- 文档（PDF / Word / PPT）
- 网站内容抓取（Web Scraping）
- 数据库
- 内部 Wiki

### 2. 处理流程
- 清洗（Cleaning）
- 切分（Chunking）
- 向量化（Embedding）
- 索引（Indexing）

### 3. 向量数据库
- FAISS
- Milvus
- Pinecone
- Weaviate
- Qdrant

### 4. RAG （检索增强）
- Naive RAG
- Hybrid Search
- Agentic RAG
- Graph RAG
向量数据库 (给AI配个图书馆)
Embedding 模型
切片与清洗
GraphRAG (知识图谱)


---

## 八、AI 编程（AI for Coding）

### 1. 编程助手
- GitHub Copilot
- Cursor
- Codeium
- ChatGPT Code Interpreter

### 2. 能力场景
- 代码生成
- 代码补全
- 代码重构
- Bug 定位
- 自动写测试

### 3. DevOps + AI
- 自动生成 CI/CD
- IaC（Terraform + AI）
- 日志分析

---

## 九、自动化工作流（Automation & Agent）

规划 (脑子好使): CoT, ReAct
记忆 (记性好): 长期/短期记忆
工具调用 (手脚麻利)
多智能体 (团队协作 CrewAI)

让 AI 不止会聊天，还能帮你干活！比如 **CrewAI** 就像雇了一群 AI 员工互相配合，**LangChain** 是把各种工具串起来的胶水。

### 1. Agent 开发框架
- LangChain
- LlamaIndex
- AutoGPT
- CrewAI
- MetaGPT
LangChain (万能胶水)
LlamaIndex (数据管家)
Semantic Kernel
Dify (拖拉拽就能做)

### 2. 工作流工具
- n8n
- Zapier
- Make
- Airflow

**神器**: **n8n** (超强，还能自己部署)，**Zapier** (简单好用)，**Dify** (小白也能搭应用)。

### 3. 典型流程
- 抓取网站 → 清洗 → 生成文章 → 发布博客
- 数据 → 分析 → 报告 → 邮件
- 视频素材 → 剪辑 → 配音 → 发布

---

## 十、应用层（Applications）

AIGI 内容生产：
自动写爆款文
营销文案一键生成
做号矩阵
多媒体创作：
数字人/视频剪辑 (HeyGen)
视频一键总结
AI 播客
企业效能：
企业知识库 (啥都懂的客服)
AI 编程搭子 (Cursor)
自动化流水线 (n8n/Zapier)
垂类行业：
K12 辅导 (苏格拉底式教学)
法律/医疗小助手
金融研报分析

### 1. 内容创作
- AI 博客系统
- AI 媒体站
- 自动化内容农场（SEO）

### 2. 视频与新媒体
- 视频号 / YouTube 自动化
- 视频简报系统
- 教学视频生成

### 3. 教育（K12 重点）
- AI 作业辅导
- 个性化学习路径
- 自动出题 / 判题
- 教师备课助手
- 学习行为分析

### 4. 企业应用
- 智能客服
- 企业知识助手
- AI 销售助手
- AI HR


AI 编程搭子 (AI Coding)
程序员福音: Cursor (现在公认最好用的 AI 编辑器)，还有 GitHub Copilot。
Devin 类: 这种更猛，直接像个真人工程师一样帮你修 Bug。


爬虫与数据清洗 (Web Scraping & ETL)
工具: Firecrawl 和 Crawl4AI 超好用，直接把花里胡哨的网页变成 AI 喜欢看的 Markdown 格式。
流程: 抓网页 -> 洗掉广告和废话 -> 切成小块 -> 存进数据库。


内容创作与营销 (Content Generation)
写文章: 扔个关键词，AI 自动去调研、列大纲，最后用 Claude 写出一篇 SEO 满分的文章。


搞视频:
数字人: HeyGen 能让照片开口说话，口型都对得上。
视频总结: 没时间看长视频？Whisper 转文字，LLM 提炼重点，一分钟看完一小时的内容。


K12 教育 (EdTech)
作业辅导: 以前是直接给答案，现在是像苏格拉底一样，一步步引导孩子自己想出来（拍照搜题升级版）。
私人外教: 随时随地练口语，发音不对立马纠正，还不收你几百块一节课。

---

## 十一、安全与治理（AI Safety & Governance）

### 1. 内容安全
- Prompt 注入防护
- 有害内容过滤
- 幻觉检测

### 2. 数据安全
- 脱敏
- 隐私保护
- 数据隔离

### 3. 模型治理
- 版本管理
- 可解释性
- 审计日志

---

## 十二、工程化（MLOps / LLMOps）

LLMOps: 像管服务器一样管理模型。
部署: 想在自己电脑上跑模型？Ollama 简直是神器，一行命令搞定。
评估 (Evaluation): Ragas 专门用来给 RAG 系统打分，看看它找资料准不准。
安全 (Security):
防套路: 别让用户几句话就把 AI 忽悠瘸了 (Prompt Injection)。
保隐私: 公司的机密数据、客户的手机号，千万不能传到公网模型上去 (PII 过滤)。

### 1. 模型生命周期
- 训练
- 部署
- 监控
- 回滚

### 2. 工具链
- MLflow
- Weights & Biases
- BentoML
- KServe

### 3. 性能优化
- 缓存
- Prompt 压缩
- 推理加速

---

## 十三、企业化与商业化（Enterprise & Business）

### 1. SaaS 化
- 多租户
- 计费系统
- 权限管理

### 2. 商业模式
- API 计费
- 订阅制
- 私有化部署

### 3. 组织与角色
- AI 产品经理
- Prompt Engineer
- AI 架构师
- AI 教育设计师

---

## 十四、趋势与未来方向

- Agent 化
- 多模态统一模型
- AI + 自动化企业
- AI 原生教育系统
- 人机协同（Human-in-the-loop）

---

```
    4. 工程化与Ops<br>LLMOps
      推理部署
        vLLM / TensorRT-LLM
        Ollama (本地轻松跑)
        LM Studio
      监控与评估
        LangSmith
        Ragas (给RAG打分)
        Arize Phoenix
      数据工程
        ETL 管道
        爬虫神器 (Crawl4AI/Firecrawl)
        洗数据
    5. 安全与伦理<br>Security
      安全防护
        防套话 (Prompt Injection)
        隐私打码 (PII)
        护栏机制 (Guardrails)
      合规性
        数据得留在国内
        版权不侵权
```