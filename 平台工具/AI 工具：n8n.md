
---
目录：[[AI 平台工具总览]]
上一页：
下一页：
关键词：
相关链接：[[AI 工具：n8n：常用APP的账户凭据及访问令牌]]

---

  
[AI 狂潮下的求生指南：為何只懂 ChatGPT 讓你離失業更近一步，n8n AI Agent 才是你的救命稻草](https://www.youtube.com/watch?v=rgU0mbVpg0k)
![image.png](https://repo.in4tree.com/2026/01/31_1769847012854.png)



---

# 【特点】

本地部署
免费（云端收费！）
第三方社区插件（1000+）
AI生成工作流（云端收费！试用14天）

> 注意：n8n不能提供商业服务！可以用Diffy


---

# 【同类比较：Zappier、Make，Google Opal、Agent Skills】

 最早其实我用Make搭建过，最后放弃！节点搭配不灵活！（有使用次数限制！$10/月，1万次）

[！！！！！零基础入门AI自动化 | n8n大师课 (理论介绍+功能拆解+案例讲解)](https://www.youtube.com/watch?v=fX-c9q9sxks)

![为什么选择n8n](https://repo.in4tree.com/2026/01/14_1768438262475.jpeg)  


## Agent Skills：傻瓜式工作流！提示词就可运行工作流！但费Token！速度慢！
  
[n8n要凉了？Claude Agent Skills实测对比，谁才是AI自动化之王！](https://www.youtube.com/watch?v=96LG1nms23Q)

![image.png](https://repo.in4tree.com/2026/01/30_1769845286406.png)


## Google Opal：傻瓜式工作流！

## 国内自动化平台缺点：集成的APP很少！！！

https://www.youtube.com/watch?v=JNRCuF2ihz4


---

# 【！！！AI自动生成工作流】n8n Cloud已经能自动生成工作流！效果比其它强很多！！！免费14天！可更换临时邮箱重新注册，永久免费使用！！！

  
[(n8n-mcp) AI驱动创建n8n自动化工作流 | AI-Powered n8n Automation Workflow](https://www.youtube.com/watch?v=VMu6Y8iTWng)

  
官方旗舰！n8n 超强AI助手：自动生成工作流，提效10x！
https://www.youtube.com/watch?v=Tn1k0pg2pEc

![image.png](https://repo.in4tree.com/2026/01/31_1769926361021.png)


## AI助手的两种工作模式：ASK（不消耗）、Build（消耗积分！）

![image.png](https://repo.in4tree.com/2026/01/31_1769926501409.png)

## 生成知识库RAG（需要上传知识文件PDF/CSV/JSON）

![image.png](https://repo.in4tree.com/2026/01/31_1769927365084.png)


---

# 【基本组成元素：分类、节点】
## 触发器（Trigger）

手动触发
应用事件触发（On App Event）：有很多常见的APP（如Gmail、Notion等）
定时触发（On a Schedule）
Http请求触发（On Webhook Call）
表单请求触发（On Form Submit）
对话框触发（On Chat Messaage）：对话方式查询本地专属知识库（RAG！！！）
被其它工作流调用（When Called by another Workflow）

![image.png](https://repo.in4tree.com/2026/01/31_1769849717778.png)

## 执行应用动作（Action in an app）

![image.png](https://repo.in4tree.com/2026/01/30_1769838829605.png)

### ？？？？？常用APP分类


## 数据转换（Data Transformation）

![image.png](https://repo.in4tree.com/2026/01/30_1769838644731.png)

## ！！！EditField(set)：对JSON文件中的field进行添加删除和修改

> 节点间传输数据是用JSON


## 代码（Code）：JS、Physon
## 日期时间（Datetime）

## 限制（Linit）
## 合并（Merge）
## ！！！汇总（Aggregate）：如3条合并为1条，变为一个List含3个元素

![image.png](https://repo.in4tree.com/2026/01/31_1769908419139.png)


## HTML
## Markdown
## 。。。


## 工作流（Flow）

![image.png](https://repo.in4tree.com/2026/01/30_1769839379211.png)

### ！！过滤（Filter）
### ！！条件判断（If）
### 分支处理（Switch）
### ！！循环（Loop）
### ！合并（Merge）
### 比较数据集（Compare Datasets）
### ！执行工作流（Execute Workflow）
### 错误退出（Stop and Error）
### ！等待（Wait）


## 核心功能（Core）

![image.png](https://repo.in4tree.com/2026/01/30_1769839823313.png)


### 代码（Code）：JS、Physon
### Http请求：主动向网站获取信息

### Webhook触发：如果外部网站有事件发生，主动推送消息到这个WebbookURL，从而启动工作流


# 数据库

## （云）Google Sheet
## （云）Notion
## （云）飞书

## （云、本地）nocodb：n8n自动化工作流的最佳搭档！

https://www.youtube.com/watch?v=czakQmd2NGI
![image.png](https://repo.in4tree.com/2026/01/31_1769846755073.png)

是自动化工作流的绝配

- 提供数据源和操作接口。
- 构建自动化工作流，连接各种服务。
- 实现数据同步、任务触发、通知提醒等。


## 向量数据库：`Pinecone Vector Store`


## AI

https://www.youtube.com/watch?v=k3xdSqwlFic

![image.png](https://repo.in4tree.com/2026/01/30_1769840234891.png)


### 免费AI大模型API方案：Gemini、或者OpenRouter（大模型API的聚合代理网站）

https://www.youtube.com/watch?v=mzjhST0Od5Q

![image.png](https://repo.in4tree.com/2026/01/31_1769922257704.png)



### ！！！AI Templates：使用别人做好的工作流模板


### ！！！！！AI Agent

> 如果上一节点是Chat，则选 `connected chat trigger node`，否则使用固定的提示词（Define message）

**AI Agent三个组成部件：**

- LLM大语言模型（Chat model）：集成了所有主流的LLM（如Gemini、OpenAI和DeepSeek）
- 记忆（memory）：如添加长期记忆、提高上下文理解能力
- 调用外部（Tool）：如向量数据库 `Pinecone Vector Store`
- ！！！输出格式（Output Parsers）：不要随便乱编造输出内容！

### LLM链；信息提取器；问答链；情感分析；摘要汇总链；文本分类器



---

# 【安装部署】
## 官方云端n8n Cloud（免费14天！可更换临时邮箱重新注册，永久免费使用！！！AI生成工作流！！！）

https://www.youtube.com/watch?v=VFw6l8oCxGc

## 用 Zeabur 一鍵云部署

[用 Zeabur 一鍵部署，擁有無限工作次數的自動化工具](https://www.youtube.com/watch?v=gJ7TF3Uiv1o)

## 免费云部署：run.claw.cloud（特惠：GitHub账号注册时间是超过180天，送$5！！！）

https://www.youtube.com/watch?v=UoD69nMbUsA
https://www.youtube.com/watch?v=oHvxc2t-_1w
![image.png](https://repo.in4tree.com/2026/01/31_1769922867554.png)


## ！！！本地部署

docs.n8n.io/hosting/installation/docker/#prerequisites
### npm（试验）

**安装node.js**


### docker（正式生产！）

https://www.youtube.com/watch?v=mzjhST0Od5Q

**安装终端工具Tabby，ssh访问docker** 


**挂载一个卷**：/home/node/.n8n（重启docker时数据不会丢失！）

创建挂载卷，保存工作流数据，避免重启docker后数据丢失！
`sudo docker volume create n8n_data`


```
sudo docker run -d --name n8n
-e N8N SECURE_COOKIE=false
-p
5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```



**映射端口**：5678

**设置环境变量**：输入这个n8n安全访问cookie（非SSL也可以访问·）
![image.png](https://repo.in4tree.com/2026/01/31_1769858945906.png)



## 重新指定配置文件（默认为本地sqlite文件，可用MySQL、Postgresgl、nocodb等，以确保永久保存工作流！）

https://www.youtube.com/watch?v=cVPD2AFlLIs



## 群晖NAS安装n8n（docker）：？？？对性能要求？

https://www.youtube.com/watch?v=hLS5nwCoGeg

### ！！！群晖NAS外网穿透：Tailscale安全快速的远程NAS访问（比群晖的connectID快很多！）

添加群晖套件Tailscale，注册运行Tailscale
![image.png](https://repo.in4tree.com/2026/01/31_1769898750115.png)

这样在外网的任何设备，只要同样安装了Tailscale，就可以外网访问了。


# 外网穿透（隧道）：项目同步、Google认证、Webhook回调URL

外网直连本地n8n工作流：零成本，3分钟搞定n8n内网穿透 | 新手必看！
https://www.youtube.com/watch?v=3LZRQbSygRw

隧道服务：Cloudfare、花生壳、蒲公英（收费！）


## 外网穿透：Cloudfare域名的隧道功能（反向代理）

外网直连本地n8n工作流：零成本，3分钟搞定n8n内网穿透 | 新手必看！
https://www.youtube.com/watch?v=3LZRQbSygRw
  
最佳免费本地部署方案：n8n + cloudflare 保姆级教程！一次搞定！
https://www.youtube.com/watch?v=zWJ4nC6lR7M


## 外网穿透：ngrok的隧道功能（反向代理）二级域名！
https://www.youtube.com/watch?v=EEXz30eUmqE

ngrok可以帮我们建立一个隧道
![image.png](https://repo.in4tree.com/2026/02/01_1769933055693.png)

比如在需要使用Webhook功能的时候


---

# 【保存、分享工作流】

## 方法一：导出json配置文件

## 方法二：配置文件（默认为本地sqlite文件，可用MySQL、Postgresgl、nocodb等，以确保永久保存工作流！）

https://www.youtube.com/watch?v=cVPD2AFlLIs



---

# 【第三方社区：工作流、节点】

https://n8n.io/workflows

比如：全自动人工智能视频生成和多平台发布


#  ？？？【开发第三方节点】





---
---

# 【参考】

  
[！！！！！零基础入门AI自动化 | n8n大师课 (理论介绍+功能拆解+案例讲解)](https://www.youtube.com/watch?v=fX-c9q9sxks)


---

# 【灵感】我的独有见解！增加视频特色和档次！！！！！

## Group： 多个节点组成一个功能

## ？？？每个节点应该有一个代码块（预处理、后处理）

## ？？？？？？抽象和封装：在工作流外面统一定义参数，而不是隐藏并嵌入在里面！

## ？？？？？子工作流能否做到编程中的函数调用：传参、返回值，交回控股权！
