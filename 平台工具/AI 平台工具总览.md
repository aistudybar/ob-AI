
---
目录：[[AI 全栈技术树（AI Full-Stack Tech Tree）【2026版】]]
上一页：
下一页：
关键词：
相关链接：

---

# 【国外AI开发者平台】
## ！！！Google AI Studio

是为**个人开发者**设计的、一款**基于浏览器**的免费 **AI 实验和原型设计**平台，让用户（包括开发者和非技术人员）能通过简单的自然语言指令和图形界面，快速体验和使用强大的 [Gemini 模型](https://aistudio.google.com/) 进行文本生成、**多模态**（文字、图片、代码）交互、数据处理等任务，并能将想法快速转换为可部署的应用，是探索和构建**生成式 AI** 解决方案的便捷起点！

### 1. 特点

- 非常适合长上下文处理：免费额度为100 万个token！！！
- 易于上手：无需编程基础，通过浏览器即可直观操作，非常适合新手、设计师和内容创作者。
- 快速原型设计：快速实验不同的模型和提示 (Prompt)，设计和测试 AI 应用。
- 多模态支持：能处理文本、图片和代码，实现智能问答、内容创作、代码生成等功能。
- 与 Gemini 模型深度集成：直接访问和利用 Google 最先进的 Gemini 系列模型。
- 跨平台分享：可以将生成的模型和提示分享给他人
- 生成代码和部署：生成应用原型后，可无缝过渡到更专业的 [Vertex AI 平台](https://cloud.google.com/generative-ai-studio?hl=zh-CN) 或直接使用 Gemini API 进行生产部署。
- Google 生态集成：可与 Google Drive、Google Maps 等服务结合，增强应用能力

### 2. 比较 Gemini

把 Google AI Studio 想象成一个开发者可以构建很酷的 AI 东西的工作坊，而 Gemini 应用更像是在你手机上有一个友好的聊天伙伴。这有点像拥有一个完整的厨房可以做饭和直接点外卖的区别。

当开发者想要创建他们自己的 AI 应用程序或向他们的网站和应用程序添加 AI 功能时，他们会前往 AI Studio。它拥有所有这些强大的工具和模型，他们可以玩，包括一些超级高级的，可以处理非常长的对话和复杂的任务。

### 3. 比较 Google AI Platform

[Google AI Platform](https://www.google.com/search?q=Google+AI+Platform&oq=Google+AI+Platform+%E6%AF%94%E8%BE%83+Google+AI+Studio&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIGCAEQRRhA0gEJMjgxODJqMGo3qAIAsAIA&sourceid=chrome&ie=UTF-8&ved=2ahUKEwj76rnbtZmSAxWuHEQIHecIEkoQgK4QegQIARAC) (现在主要称为 **Vertex AI**) 是一个全面的云端机器学习和生成式 AI 平台，提供端到端的模型开发、训练、部署，适合专业数据科学家和工程师；而 **Google AI Studio** 是一个基于 Vertex AI 之上的轻量级、可视化、面向 Prompt (提示词) 的快速原型设计工具，让开发者能快速实验、构建和共享基于大型语言模型（LLM）的 AI 应用，对非技术人员也友好。

简单来说，AI Studio是 Vertex AI 里的一个快速实验窗口，而 Vertex AI 是整个后台的强大工程平台
Vertex AI 是给企业用的，它有服务等级协议 (SLA)，可以预置资源，你能控制想用哪个地区，还和 Google Cloud 资源整合在一起。

如果你的目标用户只是普通的个人用户，Google AI Studio 就足够了。


## Google AI Platform（现在主要称为 **Vertex AI**，面向企业！）

- Google AI Platform允许用户使用Google Cloud进行机器学习模型的训练和部署。它提供了易于使用的界面和与Google Colab的集成，方便研究者和学生进行AI研究。
- Vertex AI 是给企业用的，它有服务等级协议 (SLA)，可以预置资源，你能控制想用哪个地区，还和 Google Cloud 资源整合在一起


## Google Colab

一个免费的、基于云端的 **Jupyter [Notebook](https://www.google.com/search?sca_esv=20541e4f21a9d7f7&sxsrf=ANbL-n6pedQwK6KfPBV7iDAH-K5ZMUnfaA%3A1769025330372&q=Notebook&sa=X&sqi=2&ved=2ahUKEwih9t76tJ2SAxWkHzQIHdrdMmIQgK4QegQIARAC&biw=1920&bih=919&dpr=1&aic=0) 环境**，让用户通过浏览器就能编写、运行 Python 代码，并利用 Google 提供的免费计算资源（包括 GPU 和 TPU），尤其适合机器学习、数据分析和教育用途，无需本地配置，极大降低了编程和深度学习的门槛。

让任何人都能在云端轻松进行 Python 编程和高性能计算，是学习和实践数据科学与机器学习的理想平台。

### 1. 特点

- **云端运行**：完全在云端执行，不占用本地电脑的资源，对电脑配置要求低。
- **无需设置**：预装了大量常用库（如 TensorFlow, PyTorch），即开即用，免去繁琐的环境安装。
- **免费计算资源**：提供免费的 GPU（图形处理器）和 TPU（张量处理器），对深度学习非常重要。
- **易于分享和协作**：像 Google Docs 一样，可以轻松与他人共享和共同编辑代码。
- **与 Google Drive 集成**：笔记本文件默认存储在 Google Drive，方便管理和访问。
- **适用性广**：适合数据科学、机器学习、数据分析、教育和快速原型开发。



## AWS SageMaker

- AWS SageMaker是一个完全托管的服务，它简化了机器学习工作流程，包括模型训练、评估和部署。SageMaker支持多种编程语言和机器学习框架。


## Microsoft Azure Machine Learning

- Azure Machine Learning是微软推出的AI开发平台，提供了模型训练、部署和管理功能，同时还支持与Azure Databricks和Jupyter Notebooks的集成。


## IBM Watson Studio

- IBM Watson Studio是一个基于云的AI开发平台，它提供了Jupyter笔记本、AI模型训练和部署功能，支持开发者进行AI应用的开发和部署。


## ！！！Hugging Face（AI界的GitHub！）

> - AI项目则与传统的计算机project不同，是在代码文件之外还需要有有神经网络的模型文件。不同于项目的代码文件只有几个KB或几个MB的大小，AI的神经网络模型权重往往都是几百MB或者几个GB。

- Hugging Face是一个开源的机器学习平台、AI研究和开发社区，它提供了Transformers，这是一个用于NLP任务的预训练模型和工具库。Hugging Face平台允许开发者轻松地复现和分享研究成果。
   
- 世界上第一个选择为众多神经网络项目建立一个AI计算框架的权重共享的网站的是美国的huggingface！！！
- 为了对标美国的huggingface，华为推出了mindspore的分享网站、阿里推出了modelscope



# 【国内AI开发者平台】

## 百度AI平台

- 百度AI平台提供了包括深度学习框架PaddlePaddle、AI模型市场、AI技术文档等在内的全面服务，支持开发者从零开始训练模型，也可以直接使用平台上的预训练模型。
## 腾讯AI Lab

- 腾讯AI Lab为开发者提供了丰富的AI算法和模型，以及AI开发工具，同时还支持模型训练和部署服务。
## 阿里云机器学习平台

 - 阿里云提供了强大的机器学习平台，支持包括大规模分布式训练、模型评估、模型部署等功能，适合需要处理海量数据的开发者。
## 科大讯飞开放平台

- 科大讯飞开放平台提供了语音识别、语音合成、语音评测、自然语言处理等AI服务，开发者可以通过简单的API调用接入这些服务。
## 旷视科技开放平台

- 旷视科技开放平台提供了包括人脸识别、图像识别在内的AI服务，支持开发者进行二次开发，构建自己的应用。


# 【三款热门大模型管理工具：AnythingLLM、Cherry Studio、Chatbox】（LLM的IDE！！！）

## AnythingLLM

是一款企业级**知识库管理**工具，内置向量数据库和文档智能问答功能，适合需要处理大量文档和构建私有知识库的用户。

如果您的主要需求是文档处理和构建私有知识库，AnythingLLM的文档智能问答和向量数据库功能将为您提供强大的支持。它适合依赖文档处理的企业、研究机构，或需要构建私有知识库的团队。

### 1. 特点

- 文档智能问答与向量数据库支持
- 本地化部署，保障数据安全·多用户管理与团队协作支持
- 强大的文档处理能力

### 2. 场合

- 企业内部文档库的自动化问答 (如员工手册、技术文档)
- 学术研究中的文献摘要与关键信息提取
- 个人用户管理海量笔记或电子书资源


## Cherry Studio

是一款**功能全面**的AI大模型管理工具，支持多模型切换、知识库管理、联网搜索等功能。它的开源特性和本地部署能力使其在数据隐私和定制化方面表现突出。其最大特点是支持**完全本地部署**。所有数据均存储在本地设备上，有效避免了云端同步可能带来的数据泄露风险。这一特性特别适合对数据隐私保护有严格要求的企业团队、研究机构和个人用户。

如果您需要多模型支持、强大的知识库管理和高度定制化功能，Cherry Studio是您的不二之选。它特别适合技术团队、多任务处理者，以及对数据隐私和功能扩展性要求较高的用户。

### 1. 特点

- 多模型自由切换(OpenAl、DeepSeek、Gemini等)
- 本地部署与数据隐私保护
- 强大的知识库管理和联网搜索功能
- 高度定制化与智能体支持

### 2. 场合

- 开发者进行多模型对比调试
- 创作者快速切换不同风格文案生成
- 企业需要兼顾数据隐私与云端高性能模型混合使用


## Chatbox

**轻量级**的对话式AI工具，专注于简洁的聊天体验和快速上手。它支持多种大模型，适合需要基础对话功能的用户。

如果您只需要一个简单的对话式AI工具，Chatbox的简洁界面和快速上手特性将满足您的需求。它适合个人开发者、教育工作者，或仅需基础对话功能的用户。

### 1. 特点

- 界面简洁，开箱即用·支持多种大模型
- 本地数据存储，保障隐私·轻量化设计，适合低配置设备

### 2. 场合

 - 个人用户快速测试本地模型生成效果
 - 开发者临时调试模型或生成简单代码片段
 - 教育场景中的教学演示工具
 

# 【本地大模型 (Local LLM)】

![image.png](https://repo.in4tree.com/2026/01/21_1769047817816.png)


## ！！！Ollama（只需CPU 即可部署！）

一个开源工具，专为在本地计算机上高效运行大型语言模型（LLM，如 deepseek-r1、qwen2.5 等）而设计。它简化了模型的下载、部署和管理流程，让用户无需复杂配置即可在本地体验和开发基于大语言模型的应用。

### 1. 特点

- 跨平台支持：提供针对 macOS、Windows（预览版）、Linux 以及 Docker 的安装指南，确保用户能在多种操作系统环境下顺利部署和使用 Ollama
- 简化部署：Ollama 目标在于简化在 [Docker](https://zhida.zhihu.com/search?content_id=242434953&content_type=Article&match_order=1&q=Docker&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjkwNjMwNDksInEiOiJEb2NrZXIiLCJ6aGlkYV9zb3VyY2UiOiJlbnRpdHkiLCJjb250ZW50X2lkIjoyNDI0MzQ5NTMsImNvbnRlbnRfdHlwZSI6IkFydGljbGUiLCJtYXRjaF9vcmRlciI6MSwiemRfdG9rZW4iOm51bGx9.vsdqsqFLMOtAxJGcrdKv9ugKO4Dj3EtCLE-dL2wcRTg&zhida_source=entity) 容器中部署大型语言模型的过程，使得非专业用户也能方便地管理和运行这些复杂的模型
- 预构建模型库：包含一系列预先训练好的大型语言模型，用户可以直接选用这些模型应用于自己的应用程序，无需从头训练或自行寻找模型源
- 模型导入与定制：可从 [PyTorch](https://zhida.zhihu.com/search?content_id=242434953&content_type=Article&match_order=1&q=PyTorch&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjkwNjMwNDksInEiOiJQeVRvcmNoIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6MjQyNDM0OTUzLCJjb250ZW50X3R5cGUiOiJBcnRpY2xlIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.p5k9wfsUsghOy-rxvFP5PK-z-3XY0_wUGaDfFnZ3uDs&zhida_source=entity) 、 [Safetensors](https://zhida.zhihu.com/search?content_id=242434953&content_type=Article&match_order=1&q=Safetensors&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjkwNjMwNDksInEiOiJTYWZldGVuc29ycyIsInpoaWRhX3NvdXJjZSI6ImVudGl0eSIsImNvbnRlbnRfaWQiOjI0MjQzNDk1MywiY29udGVudF90eXBlIjoiQXJ0aWNsZSIsIm1hdGNoX29yZGVyIjoxLCJ6ZF90b2tlbiI6bnVsbH0.o50GBTYC9lauk9tcq6b_yfPJfgUdU3_dE8o_UaFzkHY&zhida_source=entity) 、 [GGUF](https://zhida.zhihu.com/search?content_id=242434953&content_type=Article&match_order=1&q=GGUF&zd_token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ6aGlkYV9zZXJ2ZXIiLCJleHAiOjE3NjkwNjMwNDksInEiOiJHR1VGIiwiemhpZGFfc291cmNlIjoiZW50aXR5IiwiY29udGVudF9pZCI6MjQyNDM0OTUzLCJjb250ZW50X3R5cGUiOiJBcnRpY2xlIiwibWF0Y2hfb3JkZXIiOjEsInpkX3Rva2VuIjpudWxsfQ.vvKTnma26HeaYWWzUfxadHJZwmIgi8LNilpqjMPp-6U&zhida_source=entity)导入


## LM Studio


##  vLLM（faster than Ollama！）


## llama.cpp


# LangChain、Flowise（基于LangChain的可视化界面）

# langflow：0门槛0代码拖拽生成企业的专属AI大模型，专属llm会成为每个企业的标配，犹如2004年的每个企业都需要网站一样

# langchain-chatglm：本地私有化部署企业专有llm大语言模型

# Chatglm：清华；家用显卡就可运行！


# 【AI ChatBots】

https://my.feishu.cn/wiki/NQLow0opDijbzMkp3mnc887cnte

## 截止2025年，国际主流 AI 模型下的 ChatBot 能力大致排序

GPT4 Turbo / GPT-4o / Gemini 1.5 Pro / Claude 3 Opus > GPT-4 / Gemini Ultra > Gemini Pro / Llama 3 / Mistral Large / 微软 Copilot > Claude2 / Llama2 / GPT-3.5

## 国产主流 ChatBot 能力大致排序

KimiChat > 智谱清言 / 通义干问 > 百小应 / 海螺AI > 零一万物 / 跃问 / DeepSeek / 豆包 / 讯飞星火 / 天工 / 360 / 文心一言


# 【爬虫与数据清洗 (Web Scraping & ETL)】

> 流程：抓网页 -> 洗掉广告和废话 -> 切成小块 -> 存进数据库。

- 结构化提取
- 动态内容处理
- 反爬虫绕过

## Firecrawl、Crawl4AI、Crawlee（网页内容=》Markdown！）


## Scrapy + Playwright + Readability、Jina AI Reader（洗掉广告和废话！）



# 【AIGC 文本】

## ！！！==Claude  Sonnet== （生成文章、创意写作的最佳！完爆 ChatGPT！)


## ！！！==Google Gemini Pro==（最像人话！）


## Jasper AI、Anyword（生成SEO优化内容的能力！）

是一款写作助手，用于生成长篇内容、博客文章、广告文案、电子邮件营销活动等，支持30 多种语言。

### 1. 特点

- SEO友好的内容：理解搜索引擎优化的重要性，Jasper.ai旨在创建SEO导向的内容，有助于提高你的在线可见性并为你的网站带来有机流量。


## Copy.ai

是一款基于人工智能的写作工具，利用自然语言处理（NLP）技术，帮助用户快速生成各种营销和创意文案，如广告、社交媒体帖子、博客文章、产品描述和邮件内容等，通过提供大量模板和定制化选项，提高内容创作效率和质量。它支持多种语言，有免费和付费方案，核心功能包括多场景文案生成、语气风格控制、博客大纲创建、即时信息获取（Chat功能）等，是内容创作者和营销人员的高效助手。

### ？？？比较 ChatGPT


### 1. 特点

- **内容生成**: 快速生成博客文章、广告文案、产品描述、社交媒体帖子、邮件等。
- **模板丰富**: 超过90种模板，覆盖博客、广告、电商、社交媒体等多种场景。
- **语气和风格控制**: 可根据品牌需求调整内容语气。
- **博客工具**: 帮助生成文章大纲、段落，并可从关键词生成内容。
- **即时聊天 (Chat)**: 能够读取URL获取实时信息，生成基于最新数据的文案。
- **多语言支持**: 支持多种语言的文案生成与翻译。
- **项目管理**: 集中管理所有文案创作，方便归类和查找。 

### 2. 场景

- **数字营销**: 快速制作广告创意、落地页文案。
- **社交媒体**: 生成引人注目的帖子、标题，管理发布。
- **内容营销**: 创作博客文章、故事、新闻稿等。
- **商务沟通**: 撰写邮件、报告、演讲稿等。


# 【AIGC 图像】

## ==DALL-E== 3


## ==Midjourney==


## ==StableDiffusion==

https://stability.ai/ (需施展魔法)推荐指数：*米***
公认的 AI 绘画界的安卓，能力强大支持 controlnet、lora，可以自已炼丹也有丰富的开源模型，但是安装过程极其麻烦！开发大佬们都表示头疼，普通人更别提了，实在想用在小破站搜秋叶 aaaki 有整合版本，会方便很多推荐搭载在 ComfyUI 来使用，可以用 SD 制作复杂的自动化的工作流程。
网友部署的: https://sd3.dawn-e.cn/
ComfyUI:一个基于节点工作流的 Stable Diffusion 图形界面，通过将 Stable Diffusion 算法模块化，实现了更高效的图像生成和资源利用。最强大和模块化稳定的扩散 GUI、api 和后端，带有图形/节点界面。适用于任何想要使用 SD 制作复杂工作流程或想要了解更多 SD 工作原理的人。
参考资料一
目ComfyUI 简介
目1.9 ComfyUI 工作流


## ==FLUX==

https://fluxai.art

是一款由 Black Forest Labs 开发的开源 AI 图像生成工具，采用先进的"流匹配"技术，能够从文本描述中生成高质量、细节丰富的图像，特别擅长处理复杂场景和人物细节，推荐给需要高精度图像生成的设计师和艺术家使用。

## Ideogram

https://ideogram.ai/t/explore

是一款由前 Google Brain 员工创立的 AI 图像生成工具，能够根据文本描述生成高质量图像，特别擅长精确嵌入文本内容，支持多种风格选择（如写实、设计、3D、动浸等），推荐给需要快速生成海报、Logo 和其他视觉内容的设计师和内容创作者使用。


## ！！！==Z-Image==（免费！速度快！显存低！画质超强！替代FLUX！）+ Comfyui

https://www.youtube.com/watch?v=YY5DmWB37Nw
  
ComfyUI 結合 Z-Image Turbo 全攻略｜不可思議的6B本機生圖模型，20秒出圖、支援中文
https://www.youtube.com/watch?v=qHqRSXB4xPQ

是2025年底、**阿里推出的一个本地运行、强的可怕的图像生成模型**，有60 亿个参数。 它目前有三个变体： 🚀 Z-Image-Turbo – Z-Image 的精简版，只需8 个NFEs（函数评估次数）就能达到或超越领先的竞争对手。 它在企业级H800 GPU 上提供⚡️亚秒级推理延迟⚡️，并且可以轻松适应16G VRAM 消费级设备。

![image.png](https://repo.in4tree.com/2026/01/21_1769032135551.png)


### 1. 特点

- 本地运行
- 显存要求低：N卡 8GB以上，推荐16GB以上（N4060/4070Ti）
- 生图速度快！质量超强！
- 复杂语义和逻辑，生成故事图、九宫格、小红书等
- 从图片中生成提示词！理解能力超强！
- 字型字体都能处理好
- 中文提示词理解能力强！
- 东方审美强！如水墨画
- 人物真实感强，难分真假！达到一线商业模型的效果
- 名人辨识度高：提供名字和提示词，生成相应的图片
- 动画漫画
- 生成18无码图片！

### 2. 缺点

- 比较难安装！

安装开源主流绘图架构：Comfyui

### 比较Midjourney、FLUX



# 【AIGC 音频】（TTS、配音）

## ！！！==ElevenLabs==

提供尖端的_AI_语音合成技术，让您轻松创建逼真、富有表现力的人工智能声音。支持多语言、声音克隆和实时语音生成，适用于有声读物、配音和内容创作。


# 【AIGC 视频】

## ==Runway==


## ==Sora==-likes


## ==HeyGen==（能让照片开口说话，口型都对得上！）


## LTX Studio（角色一致性！）

是一款由以色列[Lightricks](https://www.google.com/search?q=Lightricks&sca_esv=2c168abcc81bc14b&sxsrf=ANbL-n7Oco1Vpo_N2NabWXiS9-HFYkfsyw%3A1768978975429&ei=H3pwaaH7GbGgkPIPgrOMgAk&oq=LTX+Studio+%E6%98%AF+%E4%BB%80%E4%B9%88&gs_lp=Egxnd3Mtd2l6LXNlcnAiFUxUWCBTdHVkaW8g5pivIOS7gOS5iCoCCAAyCBAAGAoYKhgeMgUQABjvBTIFEAAY7wUyCBAAGIAEGKIEMggQABiABBiiBDIFEAAY7wVI3hZQ3QxY3QxwAXgBkAEAmAF5oAF5qgEDMC4xuAEByAEA-AEC-AEBmAICoAKHAcICChAAGLADGNYEGEeYAwCIBgGQBgqSBwMxLjGgB-cBsgcDMC4xuAeAAcIHAzItMsgHCoAIAA&sclient=gws-wiz-serp&mstk=AUtExfBOKEpP3SZC7Zd19JtEpdkqReKxTcvfaCISK6zBuarvkeHjmnmASCdPMqeAyUw5vfh8NYOoMEBXJ0QEegn4uoCGorHBObFLCgaGSGeD-vyVdXOdNq6HYwD8Wr49XXeG6PN495I4ZC0EGAD3wK0Ppmbk1DeWtsgJQ3R_lpDK9eC8tVM3NrL_e7jjusAAWWx7dAMN9AvasyQA-Mlt813Y3Wlpf7kh4QiaVTz1QGk2C5O7191fYTtBobWMLLOGBvF11h3RWvtmP1XXa11QIAumxc9FQLLZlqp9g58oUlZ3dqm46w&csui=3&ved=2ahUKEwiJl4nUiJySAxVpEEQIHUdbL7oQgK4QegQIARAB)公司开发的**生成式AI电影制作平台**，它能将简单的**文本描述转化为微电影视频**，并提供可视化的编辑工具，让用户能精确控制镜头、角色、场景一致性、灯光等，实现从创意到成品的**一站式视频创作流程**，极大地降低了专业级视频制作的门槛


## Captions（短视频生成）


## ==即梦==

https://jimeng.jianying.com/

抖音剪映团队推出的文生视频大模型：除了生成视频，该网站还支持文生图、图转视频等功能


## ==可灵可图==

https://klingai.kuaishou.com/text-to-image

是一款由快手推出的AI生图工具，具备文生视频、图生视频等主要功能，特色在于其轻量化设计和不受设备限制的网页版使用，推荐理由是其便捷性和高效性，适合日常设计需求。

## 奇域AI

http://www.qiyuai.net/apps/met/loginLanding

是一款专注于中式审美的AI绘画创作平台，提供丰富的绘画风格（如水墨画、国漫、刺绣等）、智能生成艺术作品、风格延伸与微调功能，界面简洁易上手，适合艺术爱好者和专业创作者，推荐理由是其深厚的中国文化元素和高效的创作流程。


# 【音频或视频生成文本】

## ！！！Whisper（没时间看长视频？Whisper 转文字！）


## ？？？Video Briefing（视频简报制作）


## FFmpeg（为视频加字幕！）


## Descript（影音转文字！）

是**一款線上影片剪輯軟體**，能夠將影音中的語音轉換為文字，讓用戶透過編輯文字內容的方式來編輯影音，其最大的特色就是提供AI剪輯的功能，讓影音內容的編輯變得更加直覺和高效。 用戶可以在Descript中使用直觀的方式剪輯，貼上和刪除文案，相應的影像或聲音內容也會隨之被修改


# 【AI 自动化工作流】

## ==n8n== (超强、免费、本地部署！)


## ==Zapier== (简单好用！)


## Make


## Dify (小白也能搭应用！)


## Airflow


## ==Coze==（扣子）



# 【AI 编程 (AI Coding)】

## ！！！==Cursor== (现在公认最好用的 AI 编辑器！)


## GitHub Copilot


## Codeium


## ChatGPT Code Interpreter


## Devin（这种更猛，直接像个真人工程师一样帮你修 Bug！）

### 1. 比较 Cursor

Devin 是一款用于**端到端**任务的自主人工智能软件工程师，而 Cursor 是一款人工智能驱动的**代码编辑器**，它充当智能结对编程助手，可在您的集成开发环境（例如 VS Code）中提供**实时帮助**，从而实现迭代开发。

两者的关键区别在于**自主性**与**控制权**：Devin 可以**独立处理整个项目**（就像一个虚拟实习生），非常适合委派任务；而 Cursor 则让开发人员深入参与到编码过程中，提供即时反馈并保持控制权，因此更适合**日常编码**和**增量改进**。


## V0.DEV UI Gen（Vercel发布基于AI的UI代码生成服务！)




