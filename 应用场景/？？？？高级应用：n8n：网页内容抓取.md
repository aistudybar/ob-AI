
---
目录：[[AI 平台工具总览]]
上一页：
下一页：
关键词：
相关链接：

---

  
# 【n8n应用：网页内容抓取】Webhook（资讯网页URL）、AI生成150字摘要、推特文案（少于280字）、生成Linkedin专业语气版本、写入Notion、发送Telegram

https://www.youtube.com/watch?v=VFw6l8oCxGc


![image.png](https://repo.in4tree.com/2026/01/31_1769920542728.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769920742577.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769920848961.png)

AI 提示词：Expression

你是一个专业的内容编辑。请基于以下网页内容，生成三个版本的摘要：
网页内容：
{{ $('Extract HTML Content').item.json.html }}
请按以下JSON格式输出（必须是有效的JSON）：
"summary”：“150字以内的中文摘要”，
"twitter”："280字符以内的Twitter版本（适合社交媒体，简洁有题）”
"Linkedin"：“专业语气的LinkedIn版本（适合职场分享，体现专业性）
注意：
1.确保输出是有效的JSON格式
2.summary必须在150字以内
3.twitter必须在280字符以内
4.linkedin要体现专业性和深度


Code节点：格式化数据

Notion节点：保存到数据库（也可以Append a block）

Telegram节点：发送
![image.png](https://repo.in4tree.com/2026/01/31_1769921091912.png)


