
---
目录：
上一页：
下一页：
关键词：
相关链接：

---

> AI 全栈技术树（AI Full-Stack Tech Tree），覆盖从底层算力 → 模型 → 能力 → 应用 → 安全 → 工程化 → 企业化等。包含常见的AI概念、术语、工具、平台，尤其关注当前求职市场的稀缺职位（如AI工程师）、赚钱副业，如提示词、AIGC、知识库、AI编程、自动化工作流、网站内容抓取、博客文章生成、视频创作、视频简报、K12辅助教育等


## 一、底层算力层（Compute & Infrastructure）

### 1. 硬件算力芯片

- CPU：x86（==Intel== / ==AMD==）、ARM（Apple Silicon、Ampere）
- ==GPU==：==NVIDIA==（A100 / H100 / L40）、AMD MI 系列，Consumer GPU（！！！==RTX5090/4090/3090==）
- 量子计算：IBM Q、Google Sycamore
- ==ASIC==（AI 专用加速芯片）：
	- ==TPU==（神经处理器 ）：Google
	- NPU（张量处理器 ）：Ascend（华为昇腾）、Apple Neural Engine
	- LPU（语言处理器）：Groq
	- FPGA（Field-Programmable Gate Arrays）：Xilinx（now part of ==AMD==）
	- Edge AI（边缘计算）：Jetson、RK、Raspberry Pi（树莓派） + AI 加速模块
	- 移动端NPU优化：Qualcomm Hexagon、Apple Neural Engine



### 2. 云平台（不想自己买显卡就租它们的！）

- 国际：==Google Cloud Platform== (谷歌云平台)、AWS、Azure、OCI（Oracle Cloud Infrastructure，即甲骨文的云服务平台）
- 国内：阿里云、腾讯云、华为云、火山引擎
- 私有云 / 混合云：OpenShift AI、Kubeflow、NVIDIA DGX
- 专用云（一站式AI应用部署平台！）
	- ==Google Cloud== - ==Vertex AI== on Google Cloud
	- AWS Bedrock
	- Azure ==OpenAI==
	- 华为云
	- RunPod
	- Modal
	- ==！！！Hugging Face==（AI界的GitHub！）
	- ModelScope（魔搭社区，对标外网的Hugging Face！）
	- Mindspore：华为


### 3. 本地模型 (Local LLM)

- ==！！！Ollama==
- LM Studio
- vLLM（faster than Ollama！）
- llama.cpp


---

## 二、系统与基础软件层（System & Foundation）

### 1. 操作系统

- Linux（==Ubuntu== / CentOS / Rocky）
- 容器 OS（COS、Bottlerocket）

### 2. 容器与调度

- ==Docker==
- Kubernetes（K8s）
- Helm
- KubeFlow

### 3. 加速与并行

- CUDA / ROCm
- ！！！==PyTorch== （炼丹炉框架，大家基本都在用 PyTorch，Google 家的 TensorFlow 和 JAX 也有人用）
- NCCL
- DeepSpeed
- Ray


---

## 三、模型层（Model Layer）

### 1. 模型类型

- LLM（大语言模型）
- VLM（视觉语言模型）
- Diffusion（扩散模型）
- Multimodal（多模态）

### 2. 模型能力

- 文本生成
- 代码生成
- 图像生成
- 视频生成
- 音频生成

### 3. 主流模型家族

- **通用大模型**

	- ==ChatGPT==（OpenAI）
	- ==Claude==（Anthropic，写代码超强！）
	- ==Gemini==（Google）
	- ==LLaMA==（Meta）

- **开源模型**

	- ==LLaMA==（Meta）
	- Mistral / Mixtral
	- InternLM
	- Yi

* **推理模型**

	* ==GPT==-5.2
	* ==Gemini== 3 Pro
	* ==Claude== Opus 4.5 Extended Thinking
	* ==Grok== 4.1 Thinking
	* Magistral Medium v1.2
	* ==字节豆包==
	* ==文心一言==
	* ==腾讯混元==

- **多模态模型**

	- 画图：==Midjourney== （审美无敌！）、==Stable Diffusion==（WebUI/ComfyUI）、==DALL-E==、Flux
	- 做视频：==Sora==、==Runway==、Pika 1.0、Kling（快手的可灵）
	- 听与说：==ElevenLabs==、Whisper（听写超准！）、ChatTTS（说话跟真人似的）、 XTTS，Suno v3、Voice Engine

- **领域专用模型**

	- 代码：GitHub Copilot, Codeium, Tabnine
	- 科学：AlphaFold 3, GNoME, ESM3
	- 医疗：Med-PaLM 2, BioGPT

- **中文模型**

	- ==DeepSeek==
	- ==Qwen==（阿里的通义千问）
	- 文心一言（百度）
	- 混元大模型（腾讯）
	- ==字节豆包==
	- ==Kimi==
	- GLM（智谱）
	- 百川


---

## 四、模型训练与微调（Training & Tuning）

### 1. 训练方式

- Pre-training（预训练）
- SFT（指令微调，老师傅带徒弟！）
- RLHF / RLAIF（按人类喜好调整！）
- PEFT (！！！省钱微调法 ==LoRA==)

### 2. 轻量化微调（让模型学会特定领域的知识或语气！）
- ==LoRA== / QLoRA
- Axolotl
- Adapter
- ==Prompt Tuning==
- Hugging Face Transformers

### 3. 模型压缩
- Quantization（INT8 / INT4）
- Pruning
- Distillation（==蒸馏==）


---

## 五、AI 核心能力层（AI Capabilities）

### 1. 自然语言理解能力

- NLU / NLG：意图识别、情感分析、实体抽取
- 文本总结汇总
- 翻译 / 改写
- 语义搜索

### 2. 知识与推理

- Chain of Thought
- Tree of Thought
- Tool Calling
- Function Calling
- 逻辑推理: 数学解题、代码调试
- 规划能力: 任务分解、工作流编排
- 工具使用: API调用、浏览器操作、软件控制

### 3. 多模态能力

- OCR
* 视觉理解（VQA）：图像描述理解、图文关联、物体检测、场景理解
- 视频理解、视频语义分析
- 语音识别（ASR）

### 4. 提示词工程（Prompt Engineering，解锁 AI 潜力的钥匙！）

示例结构：

- **你是谁 → 扮演专家角色**    
- **你要干什么 → 清晰任务定义**    
- **你需要什么材料 → 输入数据**    
- **你不能做什么 + 必须满足什么 → 明确约束**    

常见模板：

- Zero-shot    
- One-shot / Few-shot    
- Chain-of-Thought (CoT)    
- ReAct    
- Tree-of-Thought    
- Self-Consistency    
- Multi-Agent Prompt    
- Meta Prompting


---

## ？？？六、AIGC 能力层（重点！！！）

2. 生成能力
   - 文本生成: 文章、代码、对话、创意写作
   - 图像生成: 文生图、图生图、图像编辑
   - 音视频生成: 语音合成、音乐创作、视频剪辑
   - 3D/XR内容生成

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

## 七、知识库与 RAG（重点！！！）

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

### 3. 向量数据库（Vector DBs，给AI配个图书馆！）

- FAISS
- Milvus
- Pinecone
- Weaviate
- Qdrant

### 4. RAG （检索增强，解决大模型幻觉、利用私有数据的核心技术！）

- Naive RAG
- Hybrid Search
- Agentic RAG
- Graph RAG（知识图谱，微软）


---

## 八、AI 编程（AI for Coding）（重点！！！）

### 1. 编程助手

- ==GitHub Copilot==
- ==Cursor==
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

## ？？？九、自动化工作流（Automation & Agent）（重点！！！）

规划 (脑子好使): CoT, ReAct
记忆 (记性好): 长期/短期记忆
工具调用 (手脚麻利)
多智能体 (团队协作 CrewAI)

让 AI 不止会聊天，还能帮你干活！比如 **CrewAI** 就像雇了一群 AI 员工互相配合，**LangChain** 是把各种工具串起来的胶水。

### 1. Agent 开发框架
- LangChain (万能胶水)
- LlamaIndex(数据管家)
- AutoGPT
- CrewAI
- MetaGPT
- LangGraph
- OpenAI Assistants API
- Semantic Kernel
- Dify (拖拉拽就能做)
- Vercel AI SDK
- Streamlit

### 2. 工作流工具
- n8n (超强，还能自己部署)
- Zapier (简单好用)
- Make
- Dify**Dify** (小白也能搭应用)
- Airflow
- Coze（扣子）

### 3. 典型流程
- 抓取网站 → 清洗 → 生成文章 → 发布博客
- 数据 → 分析 → 报告 → 邮件
- 视频素材 → 剪辑 → 配音 → 发布

---

## ？？？十、应用层（Applications）（重点！！！）

### AI 内容创作（AIGI）
AIGI ：批量生成高质量 SEO 文章、社交媒体内容。

Jasper
Copy.ai
Claude (Writing)
Midjourney (Images)

### AI 视频创作
HeyGen (数字人)
CapCut AI
Runway
Sora-likes

### AI 辅助编程
Cursor
GitHub Copilot
v0.dev (UI Gen)

### K12 & 教育辅助

GPT-4o (Voice)
Duolingo Max
Custom GPTs

### 智能爬虫 & 数据清洗
Crawlee
Firecrawl
Jina AI Reader


1. AIGC内容创作
   ├─ 文本内容
   │  ├─ 博客/文章生成 (如Jasper, Copy.ai)
   │  ├─ 营销文案优化
   │  └─ 小说/剧本创作
   ├─ 视觉内容
   │  ├─ 设计素材生成
   │  ├─ 产品原型图
   │  └─ 艺术创作
   └─ 视频内容
       ├─ 短视频生成 (Captions, HeyGen)
       ├─ 教育培训视频
       └─ 企业宣传片

2. 知识管理与问答
   ├─ 智能知识库构建
   │  ├─ RAG架构 (检索增强生成)
   │  ├─ 向量数据库: Pinecone, Weaviate, Milvus
   │  └─ 文档处理: LangChain, LlamaIndex
   ├─ 企业文档助手
   └─ 个人知识管家

3. AI编程与开发
   ├─ 代码生成与补全
   ├─ 代码审查与优化
   ├─ 自动化测试生成
   └─ 文档生成

4. 自动化工作流
   ├─ 智能办公自动化
   │  ├─ 邮件智能处理
   │  ├─ 会议纪要生成
   │  └─ 报告自动生成
   ├─ 业务流程自动化
   └─ 数据ETL管道

5. 内容抓取与处理
   ├─ 智能网页抓取
   │  ├─ 结构化提取
   │  ├─ 动态内容处理
   │  └─ 反爬虫绕过
   ├─ 多源数据整合
   └─ 内容清洗与标注

6. 教育应用 (K12及高等教育)
   ├─ 个性化学习助手
   │  ├─ 自适应习题推荐
   │  ├─ 知识点讲解
   │  └─ 错题分析
   ├─ 教师辅助工具
   │  ├─ 课件生成
   │  ├─ 作业批改
   │  └─ 学情分析
   └─ 语言学习
       ├─ 口语练习
       ├─ 写作批改
       └─ 沉浸式学习环境


??????????????

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
- Prompt Injection（提示词注入防护）
- Guardrails（护栏机制）
- 幻觉检测

### 2. 数据安全
- 脱敏
- PII（隐私保护）
- 数据隔离

### 3. 模型治理
- 版本管理
- 可解释性
- 审计日志


---

## 十二、工程化（MLOps / LLMOps）

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

