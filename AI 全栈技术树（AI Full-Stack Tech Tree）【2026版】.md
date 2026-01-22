
---
目录：
上一页：
下一页：
关键词：
相关链接：[[0 ？？？AI 应用场景总览]]

---

> AI 全栈技术树（AI Full-Stack Tech Tree），覆盖从底层算力 → 模型 → 能力 → 应用 → 安全 → 工程化 → 企业化等。包含常见的AI概念、术语、工具、平台，尤其关注当前求职市场的稀缺职位（如AI工程师）、赚钱副业，如提示词、AIGC、知识库、AI编程、自动化工作流、网站内容抓取、博客文章生成、视频创作、视频简报、K12辅助教育等


## 一、底层算力层（Compute & Infrastructure）

### 1. 硬件算力芯片

- CPU：x86（==Intel== / ==AMD==）、ARM（Apple Silicon、Ampere）
- ==GPU==：==NVIDIA==（A100 / H100 / L40）、AMD MI 系列，Consumer GPU（==RTX5090/4090/3090==）
- 量子计算：IBM Q、Google Sycamore
- ==ASIC==（AI 专用加速芯片）：
	1) ==TPU==（神经处理器 ）：Google
	2) NPU（张量处理器 ）：Ascend（华为昇腾）、Apple Neural Engine
	3) LPU（语言处理器）：Groq
	4) FPGA（Field-Programmable Gate Arrays）：Xilinx（now part of ==AMD==）
	5) Edge AI（边缘计算）：Jetson、RK、Raspberry Pi（树莓派） + AI 加速模块
	6) 移动端NPU优化：Qualcomm Hexagon、Apple Neural Engine


### 2. 云平台（不想自己买显卡就租它们的！）

- 国际：==Google Cloud Platform== (谷歌云平台)、AWS、Azure、OCI（Oracle Cloud Infrastructure，即甲骨文的云服务平台）
- 国内：阿里云、腾讯云、华为云、火山引擎
- 私有云 / 混合云：OpenShift AI、Kubeflow、NVIDIA DGX
- 专用云（一站式AI应用部署平台！）
	1) ==Google Cloud== - ==Vertex AI== on Google Cloud
	2) AWS Bedrock
	3) Azure ==OpenAI==
	4) 华为云
	5) RunPod
	6) Modal
	7) ==！！！Hugging Face==（AI界的GitHub！）
	8) ModelScope（魔搭社区，对标外网的Hugging Face！）
	9) Mindspore：华为


### 3. 本地模型 (Local LLM)

- ==Ollama==
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
- ==PyTorch== （炼丹炉框架，大家基本都在用 PyTorch，Google 家的 TensorFlow 和 JAX 也有人用！）
- NCCL
- DeepSpeed
- Ray


---

## 三、模型层（Model Layer）


![AI学习](https://repo.in4tree.com/2026/01/15_1768521985469.png)


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

	1) ==ChatGPT==（OpenAI）
	2) ==Claude==（Anthropic，写代码超强！）
	3)  ==Gemini==（Google）
	4) ==LLaMA==（Meta）

- **开源模型**

	1) ==LLaMA==（Meta）
	2) Mistral / Mixtral
	3) InternLM
	4) Yi

* **推理模型**

	1) ==GPT==-5.2
	2) ==Gemini== 3 Pro
	3) ==Claude== Opus 4.5 Extended Thinking
	4) ==Grok== 4.1 Thinking
	5) Magistral Medium v1.2
	6) ==字节豆包==
	7) ==文心一言==
	8) ==腾讯混元==

- **多模态模型**

	1) 画图：==Midjourney== （审美无敌！）、==Stable Diffusion==（WebUI/ComfyUI）、==DALL-E==、Flux
	2) 做视频：==Sora==、==Runway==、Pika 1.0、Kling（快手的可灵）
	3) 听与说：==ElevenLabs==、Whisper（听写超准！）、ChatTTS（说话跟真人似的）、 XTTS，Suno v3、Voice Engine

- **领域专用模型**

	1) 代码：GitHub Copilot, Codeium, Tabnine
	2) 科学：AlphaFold 3, GNoME, ESM3
	3) 医疗：Med-PaLM 2, BioGPT

- **中文模型**

	1) ==DeepSeek==
	2) ==Qwen==（阿里的通义千问）
	3) 文心一言（百度）
	4) 混元大模型（腾讯）
	5) ==豆包==（字节）
	6) ==Kimi==
	7) GLM（智谱）
	8) 百川


---

## 四、模型训练与微调（Training & Tuning，让模型学会特定领域的知识或语气！）

### 1. 训练方式

- Pre-training（预训练）
- SFT（指令微调，老师傅带徒弟！）
- RLHF / RLAIF（按人类喜好调整！）
- PEFT (！！！省钱微调法 ==LoRA==)

### 2. 轻量化微调

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
- 工具使用：API调用、浏览器操作、软件控制

### 3. 多模态能力

- `OCR`
* 视觉理解（VQA）：图像描述理解、图文关联、物体检测、场景理解
- 视频理解、视频语义分析
- 语音识别（ASR）


---

## 六、提示词工程（Prompt Engineering，解锁 AI 潜力的钥匙！）

### 1. 示例结构

- 你是谁 → 扮演专家角色    
- 你要干什么 → 清晰任务定义    
- 你需要什么材料 → 输入数据    
- 你不能做什么 + 必须满足什么 → 明确约束    

### 2. 常见模板

- Zero-shot    
- One-shot / Few-shot    
- CoT（Chain-of-Thought，推理，提升逻辑&数学能力！)    
- ReAct（Reason+Act，结合工具动作！）
- ToT（Tree-of-Thought，用于解难题、多决策路径！）  
- Self-Consistency（多次推理→找最一致解！）
- Multi-Agent Prompt    
- Meta Prompting


---

## 七、知识库（KB）与检索增强（RAG，解决大模型幻觉、利用私有数据的核心技术！）

### 1. 知识来源

- ==文档==（PDF / Word / PPT）
- ==网站内容抓取==（Web Scraping）
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

### 4. ==RAG== （检索增强）

- Naive RAG
- Hybrid Search
- Agentic RAG
- Graph RAG（知识图谱，微软）


---

## 八、AI 智能体（Agent）

### 1. Agent 开发框架

- LangChain (万能胶水！)
- LlamaIndex（数据管家！）
- AutoGPT
- CrewAI
- MetaGPT
- LangGraph
- OpenAI Assistants API
- Semantic Kernel
- Dify (拖拉拽就能做)
- Vercel AI SDK
- Streamlit

---

## 九、自动化工作流（Automation）

### 1. 工作流工具

- ==n8n== (超强、免费、本地部署！)
- ==Zapier== (简单好用！)
- Make
- Dify (小白也能搭应用！)
- Airflow
- ==Coze==（扣子）


---

## 十、安全与治理（AI Safety & Governance）

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

## 十一、工程化（MLOps / LLMOps）

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

## 十二、企业化与商业化（Enterprise & Business）

### 1. ==SaaS== （Software as a Service，软件即服务）

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

## 十三、AI就业市场（Job Marketing）

### 1. AI/ML 工程师（AI / Machine Learning Engineer，最短缺！！！）

- **职责**：设计、训练和部署机器学习/深度学习模型；优化生产环境的 AI 系统。    
- **薪水（年薪 USD）**：    
    - 初级：约 $150,000–$180,000        
    - 中级：约 $180,000–$250,000        
    - 高级：$250,000+（大型科技公司可更高）        
- **备注**：这是目前市场上人才最短缺、岗位增长最快的技术角色。

### 2. AI 基础设施工程师（AI Infrastructure Engineer）

- **职责**：设计、维护 AI 平台基础架构，包括 GPU/集群调度与分布式系统。    
- **薪水（年薪 USD）**：$170,000–$260,000+    
- **价值**：支持大模型训练和推理系统的可扩展运行。

### 3. AI 数据工程师（AI Data Engineer）

- **职责**：构建和维护数据管道，为 AI/ML 模型提供清洁、可用的数据。    
- **薪水（年薪 USD）**：$160,000–$220,000+    
- **需求驱动**：数据集规模和 AI 自动化需求增加推动此岗位成为核心支持角色。

### 4. AI 产品经理（AI Product Manager）

- **职责**：将 AI 技术融入产品战略，协调技术与商业目标。    
- **薪水（年薪 USD）**：$160,000–$210,000+    
- **特点**：结合技术背景与管理能力，高度稀缺。

### 5. 机器学习研究员（AI/ML Researcher）

- **职责**：开发新算法、推动人工智能科学研究。    
- **薪水（年薪 USD）**：$150,000–$350,000+（顶尖研究机构和大厂更高）    
- **趋势**：高级研究角色需求稳健但人才稀缺。

### 6. 数据科学家（AI / ML Specialization Data Scientist）

- **职责**：数据分析、建模、特征工程与业务洞察。    
- **薪水（年薪 USD）**：$150,000–$200,000+    
- **需求**：依然是 AI 团队不可或缺的人才。

### 7. 分析工程师（Analytics Engineer）

- **职责**：构建数据层与分析流程，为 AI 系统提供高质量数据源。    
- **薪水（年薪 USD）**：$130,000–$180,000+    
- **趋势**：作为连接数据和 AI 的桥梁人才需求上升。

### 8. ==Prompt 工程师== / LLM 工程师

- **职责**：优化大型语言模型（LLM）输入与交互设计，使 AI 系统输出更准确。    
- **薪水（年薪 USD）**：$90,000–$200,000+    
- **注**：该岗位在 AI 快速部署中变得越来越重要。


---

## 十四、\$\$\$ OPC（One Person Company - ==一人公司==！！！） 盈利模式

### [[AI 全栈能力 $$$ 赚钱 $$$【2026版】]]


### 1. 接单（服务费）

- PPT
- 翻译
- 视频
- 设计

### 2. 自动运营

- SEO内容站
- 虚拟主播号

### 3. 内容变现（广告、营销联盟）

- ==Youtube视频==
- ==网站博客==

### 4. 数字产品

- 模板
- 插件
- ==教学课程==
- ==APP==

### 5. 订阅服务

- ==Email简报==
- ==SaaS==（软件即服务）


### 6 企业产品

- ==AI客服==
- ==AI专家==（专属知识库）
- AI秘书

### 7. ==AI智能体==（==Agent==）开发

- 


---

