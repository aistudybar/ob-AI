
---
目录：
上一页：
下一页：
关键词：
相关链接：

---

推理类模型


Temperature / Top-K / Top-P
幻觉（Hallucination）成因
对齐（Alignment）与偏差

向量化（Embedding）
切片与清洗

机器学习
神经网络
神经卷积

深度学习、自然语言处理、计算机视觉
自然语言生成技术（NLG）

多模态
多模态神经语言模型（如CLIP）和图像去噪扩散模型（Diffusion）

大语言模型（LLM）
AI智能体（AI Agent）

虚拟数字人

提示工程（Prompt Engineering）
https://my.feishu.cn/wiki/Qa1uwiLTVii5ockKBwRcPQnPnKb
https://www.promptingguide.ai/zh
https://platform.openai.com/docs/guides/prompt-engineering
提示工程（Prompt Engineering）是一门**向AI模型提供有效指令，使其生成理想结果的艺术**。其核心在于通过精心设计的指令，引导AI生成特定、高质量的输出，从而解锁AI的潜力。




ASIC (Application-Specific Integrated Circuit)
AI芯片定义为“专门针对AI算法做了特殊加速设计的芯片”。

在AI芯片领域，GPU既面临ASIC（如谷歌TPU）在特定场景的性能优势竞争。

GPU因为不是专门针对AI算法开发的ASIC，执行AI计算的速度优势还没到极限，还有提升空间。所以GPU不是适合智能驾驶的最佳AI芯片选择。因此开发ASIC就成了必然。

使用GPU、FPGA等已有的通用芯片可以避免专门研发定制芯片（ASIC）的高投入和高风险。


FPGA (Field-Programmable Gate Array)
提供了高度的彈性，適合產品原型開發、小批量客製化以及需要快速迭代的應用。
目前通用的CPU、GPU、FPGA等都能执行AI算法，只是执行效率差异较大。


？？？==Hugging Face== (AI界的GitHub)

https://www.cnblogs.com/xyz/p/17938629
搞AI的应该都是知道huggingface是啥的，这里不过多介绍，简单的来说就是AI模型的Github，之所以这么说是因为计算机的项目往往都是代码文件，所有计算机项目的Github只需要上传项目的代码文件即可，而AI项目则与传统的计算机project不同，是在代码文件之外还需要有有神经网络的模型文件。不同于项目的代码文件只有几个KB或几个MB的大小，AI的神经网络模型权重往往都是几百MB或者几个GB。虽然一直有人把模型权重进行网络共享，但是往往都是使用网络云盘的方式来实现，基本采用了项目代码和权重文件分开的方式，而且由于神经网络权重往往需要较大的存储空间（几百MB甚至几个GB），因此更多的人不选择公开神经网络权重的方式而只公开项目代码。虽然只公开项目代码的开源形式是最为广泛的，但是由于神经网络项目往往具有较大的随机性，也就是说能获得好用的权重往往是一个随机的事情，即使参数炼丹搞的再好也是需要运气加成的，而且往往一个神经网络项目的权重训练需要较长的运行时间和计算资源的消耗，这里比较有名的就是OpenAI的ChatGPT了，为了训练20个G的权重用了近万台服务器和显卡，训练上半年甚至一年时间，其花销是极为巨大的，也正是因此开源神经网络项目的神经网络权重一直是行业痛点。
世界上第一个选择为众多神经网络项目建立一个AI计算框架的权重共享的网站的是美国的huggingface！！！
为了构建国内的AI模型分享网站，也是为了对标美国的huggingface，华为推出了mindspore的分享网站。不限制AI计算框架的权重分享网站。
阿里公司也是在大语言模型火爆AI领域的大背景下选择跟进，推出了对标huggingface的modelscope，当然阿里的modelscope在功能上有极小一部分和华为的mindspore重叠，但是也有一些独立的服务和功能，比如是把modelscope独立为一个网站来运营，并且只做神经网络权重分享，因此和华为的mindspore还是有一定的差异性的，而且和美国的huggingface也更为相近。


---

NVIDIA的CUDA平台、AMD的ROCm平台

**平台/模型**：OpenAI API、DeepSeek、Claude、LangChain、LlamaIndex
**应用范式**：LangChain（Agent/RAG）  
**部署/运维**：Docker、Kubernetes、vLLM、TensorRT


---

## [[AIGC（Artificial Intelligence Generated Content）即人工智能生成内容]]

？？？？？