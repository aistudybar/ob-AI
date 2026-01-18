
---
目录：
上一页：
下一页：
关键词：
相关链接：

---

> 覆盖：底层算力 → 模型 → 能力 → 应用 → 安全 → 工程化 → 企业化
> 重点关注：AIGC、知识库、AI 编程、自动化工作流、网站内容抓取、博客文章生成、视频创作 / 视频简报、K12 辅助教育

---

AI 全栈技术树（AI Full-Stack Tech Tree），覆盖从底层算力 → 模型 → 能力 → 应用 → 安全 → 工程化 → 企业化等。包含常见的AI概念、术语、工具、平台，尤其关注当前求职市场的稀缺职位（如AI工程师）、赚钱副业，如AIGC、知识库、AI编程、自动化工作流、网站内容抓取、博客文章生成、视频创作、视频简报、K12辅助教育等

## 一、底层算力层（Compute & Infrastructure）

### 1. 硬件算力
- **CPU**：x86（Intel / AMD）、ARM（Apple Silicon、Ampere）
- **GPU**：NVIDIA（A100 / H100 / L40）、AMD MI 系列
- **AI 加速器**：
  - TPU（Google）
  - NPU（华为 Ascend、Apple Neural Engine）
  - FPGA（Xilinx）
- **边缘设备**：Jetson、RK、树莓派 + AI 模块

### 2. 算力形态
- 本地算力（Local AI / On-device AI）
- 私有云 / 混合云
- 公有云 GPU
- Serverless AI（按调用计费）

### 3. 云平台
- **国际**：AWS、GCP、Azure、OCI
- **国内**：阿里云、腾讯云、华为云、火山引擎
- **AI 专用云**：
  - AWS Bedrock
  - Azure OpenAI
  - Google Vertex AI

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
- **通用大模型**
  - GPT-4 / GPT-4o / GPT-5（OpenAI）
  - Claude（Anthropic）
  - Gemini（Google）
  - LLaMA（Meta）
- **中文模型**
  - 通义千问
  - 文心一言
  - 智谱 GLM
  - 百川
- **开源模型**
  - LLaMA / Mistral / Qwen / Yi

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
- 指令微调（SFT）
- RLHF / RLAIF
- Continual Learning

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

### 4. RAG 架构
- Naive RAG
- Hybrid Search
- Agentic RAG
- Graph RAG

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

### 1. Agent 框架
- LangChain
- LlamaIndex
- AutoGPT
- CrewAI
- MetaGPT

### 2. 工作流工具
- n8n
- Zapier
- Make
- Airflow

### 3. 典型流程
- 抓取网站 → 清洗 → 生成文章 → 发布博客
- 数据 → 分析 → 报告 → 邮件
- 视频素材 → 剪辑 → 配音 → 发布

---

## 十、应用层（Applications）

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

> 如果你愿意，我可以：
> - 为【某一方向】单独拆解成“学习路线图”
> - 给你一张【AI 全栈能力 × 职业发展】对照表
> - 设计【K12 / 内容创作 / 视频工厂】完整 AI 架构方案

