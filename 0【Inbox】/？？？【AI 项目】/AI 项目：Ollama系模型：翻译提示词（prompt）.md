
---
目录：
上一页：
下一页：
关键词：
相关链接：

---




[https://chat.deepseek.com/a/chat ... 5-9910-f7813cbaa62b](https://chat.deepseek.com/a/chat/s/903846c1-a103-47c5-9910-f7813cbaa62b"%20\t%20"_blank)  
  

**翻译提示词**

1. $prompt = <<<PROMPT
2. [翻译任务]
3. 源语言: {$sourceLang}
4. 目标语言: {$targetLang}
5. 专业领域: {$domain}
6. 请严格遵循以下要求:
7. 1. 保持专业术语准确
8. 2. 符合目标语言习惯
9. 3. 保留原文格式
10. 待翻译文本:
11. {$text}
12. 翻译结果:
13. PROMPT;

  
  

**专业翻译增强参数**

1. $options = [
2.     // 技术文档翻译
3.     'technical' => [
4.         'temperature' => 0.1,
5.         'stop' => ['\n\n', '术语表:'],
6.         'system_prompt' => '严格按照术语表翻译技术文档'
7.     ],

9.     // 文学翻译
10.     'literary' => [
11.         'temperature' => 0.3,
12.         'top_p' => 0.95,
13.         'system_prompt' => '保持文学韵味和修辞风格'
14.     ],

16.     // 实时对话翻译
17.     'conversation' => [
18.         'max_tokens' => 256,
19.         'frequency_penalty' => 0.2,
20.         'presence_penalty' => 0.1
21.     ]
22. ];

  

**完整API调用示例**

  
  

**特殊场景处理**

  

1. **术语一致性问题**
2. // 在prompt/message中添加术语表
3. $prompt .= "\n\n术语对照表:\nAI -> 人工智能\nLLM -> 大语言模型";

  

1. **长文本分块处理**
2. // 当文本超过2000字符时自动分块
3. $chunks = str_split($longText, 2000);
4. foreach ($chunks as $chunk) {
5.     // 发送分块翻译请求
6. }

  

1. **格式保留技巧**
2. // 在prompt中明确格式要求
3. $prompt = "保留原始Markdown格式翻译以下内容:\n```\n{$markdownText}\n```";

  
  
选择哪种参数组合取决于：  

- 使用的具体模型API
- 翻译内容的专业领域
- 对创造性/准确性的偏好
- 是否需要保持对话上下文