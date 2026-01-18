**、常用端点简介**

1. **/api/generate**: 用于生成基于单一提示（prompt）的文本完成。
2. **/api/chat**: 用于模拟对话，支持多轮消息历史。
3. **/api/embed**: 用于生成文本的嵌入向量（embedding）。
4. **/api/pull**: 从Ollama模型库下载模型。
5. **/api/show**: 查看模型的详细信息。

  
  

**二、常用参数（以/api/generate为例）**

这些参数是最常使用的，适用于大多数生成任务。

1. **model**  
    - **类型**: 字符串（String）
    - **必选**: 是
    - **功能**: 指定使用的模型名称，例如"llama3.2"、"mistral:latest"等。
    - **示例**: "model": "llama3.2"
    - **说明**: 你需要先通过ollama pull <model_name>下载模型，或者确保模型已本地可用。
2. **prompt**（/api/chat时messages）  
    - **类型**: 字符串（String）
    - **必选**: 是（仅限/api/generate）
    - **功能**: 输入的提示文本，模型将基于此生成响应。
    - **示例**: "prompt": "今天天气怎么样？"
    - **说明**: 在/api/chat中，这一参数被messages替代。
3. **stream**  
    - **类型**: 布尔值（Boolean）
    - **必选**: 否
    - **默认值**: true
    - **功能**: 控制响应是否以流式（streaming）方式返回。如果为true，响应会逐部分返回；如果为false，则一次性返回完整响应。
    - **示例**: "stream": false
    - **说明**: 流式输出适合实时应用，非流式适合需要完整结果的场景。
4. **options**  
    - **类型**: 对象（Object）
    - **必选**: 否
    - **功能**: 包含高级模型参数，用于调整生成行为。
    - **常用子参数**:  
        - **temperature**  
            - **类型**: 浮点数（Float）
            - **默认值**: 0.8
            - **功能**: 控制输出的创造性。值越高（例如1.5），输出越随机；值越低（例如0.2），输出越确定。
            - **示例**: "temperature": 0.7
        - **top_k**  
            - **类型**: 整数（Integer）
            - **默认值**: 40
            - **功能**: 在生成时只考虑概率最高的前k个候选词，限制输出范围。
            - **示例**: "top_k": 50
        - **top_p**  
            - **类型**: 浮点数（Float）
            - **默认值**: 0.9
            - **功能**: 核采样（nucleus sampling），只考虑累积概率达到p的词，增加多样性。
            - **示例**: "top_p": 0.95
        - **repeat_penalty  float**   可选，惩罚重复 token，通常设置 1.0 ~ 1.2 以减少重复文本，默认 1.1。
        - **max_tokens**  int 可选，生成文本的最大 token 数，默认 2000（可根据显存适当调整）。
    - **说明**: 这些参数调整生成文本的风格和质量。

  
  

**三、完整参数（以/api/generate和/api/chat为例）**

以下是更全面的参数列表，包括高级选项和特定场景参数。

**/api/generate完整参数**

1. **model**（见上文）
2. **prompt**（见上文）
3. **stream**（见上文）
4. **system**  
    - **类型**: 字符串（String）
    - **必选**: 否
    - **功能**: 设置系统提示，定义模型的行为或角色，覆盖模型默认设置。
    - **示例**: "system": "你是一个幽默的助手"
    - **说明**: 用于定制模型的语气或背景知识。
5. **template**  
    - **类型**: 字符串（String）
    - **必选**: 否
    - **功能**: 自定义提示模板，覆盖模型默认模板。
    - **示例**: "template": "{{ .Prompt }}"
    - **说明**: 支持变量如{{ .System }}、{{ .Prompt }}，用于精确控制输入格式。
6. **context**  
    - **类型**: 整数数组（Array of Integers）
    - **必选**: 否
    - **功能**: 上一次调用的上下文，用于保持对话连续性。从之前的响应中获取。
    - **示例**: "context": [1, 2, 3, 4]
    - **说明**: 在多轮对话中传递上下文，避免重复输入历史。
7. **images**  
    - **类型**: Base64编码的字符串数组（Array of Strings）
    - **必选**: 否
    - **功能**: 用于多模态模型（如Llava），输入图片与文本一起处理。
    - **示例**: "images": ["base64_string1", "base64_string2"]
    - **说明**: 仅对支持图像输入的模型有效。
8. **options**（高级参数，除了temperature、top_k、top_p外还有以下）:  
    - **num_ctx**  
        - **类型**: 整数（Integer）
        - **默认值**: 2048
        - **功能**: 设置上下文窗口大小，控制模型能记住的token数量。
        - **示例**: "num_ctx": 4096
    - **repeat_penalty**  
        - **类型**: 浮点数（Float）
        - **默认值**: 1.1
        - **功能**: 惩罚重复内容，值越高重复越少。
        - **示例**: "repeat_penalty": 1.2
    - **num_predict**（max_tokens）  
        - **类型**: 整数（Integer）
        - **默认值**: -1（生成直到停止）
        - **功能**: 限制生成的最大token数。
        - **示例**: "num_predict": 128
    - **stop**  
        - **类型**: 字符串数组（Array of Strings）
        - **功能**: 指定停止生成的标记。
        - **示例**: "stop": ["\n", "END"]
    - **mirostat**  
        - **类型**: 整数（Integer）
        - **默认值**: 0（禁用）
        - **功能**: 启用Mirostat采样控制困惑度（0=禁用，1=Mirostat，2=Mirostat 2.0）。
        - **示例**: "mirostat": 1
9. **keep_alive**  
    - **类型**: 整数或字符串（Integer or String）
    - **默认值**: "5m"（5分钟）
    - **功能**: 控制模型在内存中保留的时间。支持秒数（如3600）、时间字符串（如"10m"）或-1（永久保留）。
    - **示例**: "keep_alive": "10m"

**/api/chat特有参数**

/api/chat与/api/generate类似，但更适合对话场景。主要区别在于以下参数：

  
  
  
  
**messages**

- - **类型**: 对象数组（Array of Objects）
    - **必选**: 是
    - **功能**: 对话历史，包含角色和内容。
    - **子字段**:  
        - **role**: 角色（"system", "user", "assistant"）
        - **content**: 消息内容（String）

  
**示例**:json  
  
"messages": [  {"role": "system", "content": "你是助手"},  {"role": "user", "content": "你好"}]

- - **说明**: 替代prompt，支持多轮对话。

**tools**

- - **类型**: 对象数组（Array of Objects）
    - **必选**: 否
    - **功能**: 定义模型可调用的工具（如函数），仅支持兼容模型（如Llama 3.1）。  
        **示例**:json  
          
        "tools": [  {    "type": "function",    "function": {      "name": "get_weather",      "description": "获取天气",      "parameters": {        "type": "object",        "properties": {          "city": {"type": "string"}        }      }    }  }]
    - **说明**: 模型会返回工具调用建议，需后续处理。

  
  

**四、参数功能总结**

- **基本控制**: model, prompt/messages, stream 用于选择模型和输入内容。
- **输出风格**: temperature, top_k, top_p, repeat_penalty 调整生成文本的随机性和连贯性。
- **上下文管理**: num_ctx, context 控制记忆范围和对话连续性。
- **多模态支持**: images 用于图片输入。
- **高级调整**: mirostat, num_predict, stop 提供更精细的生成控制。
- **资源管理**: keep_alive 优化内存使用。

  
  

**五、注意事项**

1. **参数兼容性**: 并非所有模型支持所有参数（如tools仅限特定模型）。
2. **性能影响**: 增大num_ctx或加载多模态输入会增加内存和计算需求。
3. **默认值**: 未指定参数时，使用模型或Ollama的默认设置。