# System Prompts Atlas

System Prompts Atlas 是一个收集各种公开部署聊天机器人系统消息指令的仓库。这里汇聚了来自不同平台和模型的系统提示信息，对于研究聊天机器人行为、开发自定义聊天机器人或者仅仅是对聊天机器人背后的工作原理感兴趣的人来说，是一个宝贵的资源。

## 🌟 核心特性

- 多平台覆盖：包含OpenAI、Anthropic、Google等主流AI厂商的系统提示
- 版本追踪：记录不同模型版本的系统指令变更历史
- 安全实践：遵循OWASP安全标准进行敏感信息处理
- 开发友好：提供React组件示例和Next.js集成方案
- 持续更新：社区驱动的实时更新机制

## 📜主要内容

### 各平台系统提示文档

- **Anthropic**：包含 Claude.ai 的系统消息常见问题解答（FAQ），涵盖了从搜索指令、工具使用到处理用户反馈等多个方面的详细指南。例如，在处理复杂查询时，Claude 会根据规则进行多工具调用，像在投资策略分析场景中，会结合 Gmail、Google Drive 等工具进行研究。

    ```plaintext
    Armed with a good understanding of the restrictions, I'll review your current investment strategy to assess potential impacts. First, I'll find out where you work by reading your Gmail profile. 
    [read_gmail_profile]

    Diving into your google drive for recent investment strategy documents and holdings.
    [google_drive_search: investment strategy]

    ...
    ```

- **OpenAI**：记录了不同模型（如 o3、o4 - mini 等）的推理努力程度（reasoning_effort）和“Juice”（在开始最终响应之前允许的思维链步骤数）的对应关系，以及 Yap 分数（衡量回答详细程度的指标）的相关信息。

    | Model | reasoning_effort | CoT steps allowed before starting final response |
    | --- | --- | --- |
    | o3 | Low | 32 |
    | o3 | Medium | 64 |
    | o3 | High | 512 |
    | o4 - mini | Low | 16 |
    | o4 - mini | Medium | 64 |
    | o4 - mini | High | 512 |

### 🗂 目录结构

```bash
.
├── Anthropic/          # Claude系列系统指令
│   ├── claude-3.7-full-system-message.md
│   └── claude-sonnet-4.md
├── openai/             # ChatGPT系列配置
│   ├── chatgpt-codex.md
│   └── gpt-4o-image-safety.md
├── google/             # Gemini/Palm相关
├── docs/               # 分析报告与白皮书
├── public/             # 静态资源
└── CONTRIBUTING.md     # 贡献规范
```

## 🤝贡献指南

我们欢迎社区的贡献！如果您发现了新的系统提示信息，或者对现有文档有改进建议，欢迎提交 Pull Request（PR）。请确保在提交 PR 时引用所有非自己发现的信息来源。

## 🚀致谢与引用

- <https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools.git>
- <https://github.com/asgeirtj/system_prompts_leaks.git>
- <https://github.com/jujumilk3/leaked-system-prompts.git>
