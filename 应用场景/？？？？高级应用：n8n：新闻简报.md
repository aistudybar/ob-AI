
---
目录：[[AI 平台工具总览]]
上一页：
下一页：
关键词：
相关链接：

---


# 【常用新闻源、RSS订阅源】

Hacker News
https://www.ifanr.com/feed

Gnews
NewAPI

https://www.ifanr.com/feed（数码科技新闻）
https://www.qbitai.com/feed（ai人工智能新闻）
http：//feed.smzdm.com/（每天更新网友爆料、编辑精选的优惠信息，包括各大B2c网站的特价商品和促销活动，
https：//www.gcorescom/rss（游戏相关的新闻）

# 【n8n应用：每日新闻】获取新闻来源、翻译、发送到Telegram

[！！！！！零基础入门AI自动化 | n8n大师课 (理论介绍+功能拆解+案例讲解)](https://www.youtube.com/watch?v=fX-c9q9sxks)

![image.png](https://repo.in4tree.com/2026/01/30_1769844292262.png)

## 定时触发节点（设置时区）

## Http请求节点：2个新闻网站来源：Gnews、NewAPI

> Gnews免费版100次请求/天、每次10文章
> 获取Gnews、NewAPI的API
> URL中的q代表查询条件，如 `ai`，lang代表语言


## EditField(set)节点

因为两个新闻来源输出的JSON格式不同，为方便处理，需要用EditField(set)节点！统一为自定义JSON格式

## 合并（Merge）节点

> 注意：Merge节点不是合并数据！而是工作流

## AI节点

！！！**设置提示词**

![image.png](https://repo.in4tree.com/2026/01/30_1769842525507.png)

**设置LLM模型**：选择Gemini

**设置不强制输出格式**

测试，LOG显示得到2个输出结果（注意：Merge节点不是合并数据！而是工作流）

## ！！！Telegram节点

### 创建机器人（名称必须包含 `bot`），**获取添加认证和令牌**

打开Telegram，搜索BotFather，并对话：
![image.png](https://repo.in4tree.com/2026/01/30_1769843327339.png)

**获得Chat ID**（某人、某群组）

打开网址：
`https://api.telegram.org/{botTOKEN}/getUpdates`

与机器人对话后，再打开刚才的网址，复制其中的ID：
![image.png](https://repo.in4tree.com/2026/01/30_1769843710991.png)

**设置n8n中的Telegram节点**

![image.png](https://repo.in4tree.com/2026/01/30_1769843969113.png)



---

# 【n8n应用：自动搜集每日新闻】AI自动评选合格的新闻、生成音频日报、发送Telegram、同步到我的notion表格、然后博客会自动解析

https://www.youtube.com/watch?v=JNRCuF2ihz4

![image.png](https://repo.in4tree.com/2026/01/31_1769848663093.png)


AI自动评选合格的新闻
通过火山的语音API自动生成音频
把音频保存到AWS的存储桶里面
发送Telegram
最后把日报同步到我的notion表格，然后博客会自动解析

![image.png](https://repo.in4tree.com/2026/01/31_1769848966357.png)

> 最早其实我用Make搭建过，最后放弃！节点搭配不灵活！（有使用次数限制！$10/月，1万次）


## RSS节点（网页信息读取）

> Chrome扩展：RSSHub

如我关注的AI网站 aibase.com（提供RSS订阅）
![image.png](https://repo.in4tree.com/2026/01/31_1769850031369.png)


### ？？？？？问题：如何同时获取多个网站的RSS？

## Notion节点

![image.png](https://repo.in4tree.com/2026/01/31_1769850776698.png)

### ？？？？？添加Notion授权和密钥

## Edit Fields：把JSON数据提取后生成新的JSON数据

![image.png](https://repo.in4tree.com/2026/01/31_1769851213787.png)



## Convert to file：转换为文件（如XLS文件），并保存到本地文件夹

![image.png](https://repo.in4tree.com/2026/01/31_1769851386632.png)



---

# （无实现具体步骤！）【n8n应用：AI 自动提取长视频生成短视频 (剪辑/翻译/配音)】

  
[一个长视频链接，AI 自动生成短视频 (剪辑/翻译/配音)！我用 n8n + Gemini 搭建了自动化工厂，长视频一键变爆款](https://www.youtube.com/watch?v=A8kJ8Ddmu5Q)

## 1.AI策划：将YouTube链接发送给Gemini，生成一份详细的短视频剪辑方案（JSON格式），包含标题、描述、音乐风格以及多个待剪辑片段的时间

![image.png](https://repo.in4tree.com/2026/01/31_1769847617486.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769847955147.png)


## 2.视频制作（分支）：根据Al生成的剪辑方案，使用yt-dlp下载原始视频，然后通过FFmpeg循环剪辑出所有需要的片段，并最终将它们合并成一个天


![image.png](https://repo.in4tree.com/2026/01/31_1769848041566.png)


## 3.音频制作（分支）：根据AI生成的剪辑方案，再次调用AI生成一份与视频时长匹配的、风格化的中文配音稿，然后通过本地TTS服务生成配音。

![image.png](https://repo.in4tree.com/2026/01/31_1769847816403.png)

## 4.字幕制作（分支）：根据AI生成的剪辑方案，将其在原始视频中的时间戳转换为从O开始的相对时间轴，然后再次调用AI生成高密度的关键词字幕（VTT格

![image.png](https://repo.in4tree.com/2026/01/31_1769848067261.png)


## 5.最终合成：将制作好的无声视频、配音、背景音乐和字幕文件最终合成为一个完整的成品视频。

![image.png](https://repo.in4tree.com/2026/01/31_1769848105114.png)


## 【附】yt-dlp (视频下载工具) 

Github： [https://github.com/yt-dlp/yt-dlp](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbHBFbnNxWEZRVi03X3BKYzdpYkc3Z19TakRzZ3xBQ3Jtc0trS1JFbmJmSHVNLURfU3hyUGNlb0szNlJxUjFTME1wRFBnSEFyQVFjbFc2d0NLc1BBejVNdmNETmhNcGZsUVE1RW5kZm8zRmhMY3JKRV9BYmg2Q3pzNHBWWldrNUI3TUU4SGNUdTRkRXJOMjdWT3Zhcw&q=https%3A%2F%2Fgithub.com%2Fyt-dlp%2Fyt-dlp&v=A8kJ8Ddmu5Q)


  
# 【n8n应用：纯自动化智能新闻推荐】飞书

https://www.youtube.com/watch?v=4t6DyKwxRZM

![image.png](https://repo.in4tree.com/2026/01/31_1769853224109.png)

## 网页请求节点（网页内容抓取）：新闻汇总网站（REST API）

![image.png](https://repo.in4tree.com/2026/01/31_1769853617503.png)



## HTML节点：获取日期和URL（确保信息新鲜度！）

![image.png](https://repo.in4tree.com/2026/01/31_1769853725900.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769853858327.png)


## ！Split节点：拆分一些字段：发布时间和URL给放在一个数组里面

![image.png](https://repo.in4tree.com/2026/01/31_1769853949001.png)

## Edit Fields节点：

![image.png](https://repo.in4tree.com/2026/01/31_1769854163021.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769854188046.png)

## Switch节点：过滤24小时内的

![image.png](https://repo.in4tree.com/2026/01/31_1769854374856.png)

## Loop节点：每条数据去LLM大模型进一步优化、清洗

## HTTP节点：请求每个URL，获取网页数据

## HTML节点：清洗数据（过滤掉html标签等无用的内容）

![image.png](https://repo.in4tree.com/2026/01/31_1769854675354.png)

## AI节点：选用DeepSeek，清洗数据、打分、分类、输出格式

![image.png](https://repo.in4tree.com/2026/01/31_1769854764132.png)

## Code节点：整理数据

![image.png](https://repo.in4tree.com/2026/01/31_1769855008279.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855057747.png)



## ！！飞书：设置比较繁琐！

![image.png](https://repo.in4tree.com/2026/01/31_1769855246472.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855272981.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855323631.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855372541.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855396285.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855436134.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769855492427.png)

## 飞书节点：


## 飞书节点：表格保存和存储数据，以及定时推送

在飞书中创建一个群聊和一个机器人，实现推送信息到群聊（获取群聊Chat ID）

![image.png](https://repo.in4tree.com/2026/01/31_1769855806813.png)


