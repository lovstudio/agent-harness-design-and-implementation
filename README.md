# 主流 Agent Harness 的设计与实现

这是一本持续更新的开源小书。

我们不只评测 Agent “好不好用”，而是尽量追到 Harness 的真实实现：System Prompt 如何组装，工具如何注册，上下文如何分层，权限、记忆、Skills 和 Agent Loop 又如何共同塑造最后的 Agent。

## 目录

| Chapter | 主题 | 文章 | 可审阅材料 |
| --- | --- | --- | --- |
| 01 | System Prompt | [主流 Agent Harness 对比 01：System Prompt](chapter-01-system-prompt/) | [Codex、Claude Code、Pi 与 DSH](chapter-01-system-prompt/prompts/) |

## 仓库结构

每一期文章都是根目录下的一个独立章节：

```text
chapter-01-system-prompt/
├── README.md          # 正文
├── chapter.json      # 章节元数据
├── assets/           # 卡片、图表和插图
├── prompts/          # 可审阅的 Prompt 或 Prompt Builder 快照
│   └── index.json      # 网站同步清单
└── SOURCES.md        # 版本、来源与口径
```

后续章节沿用 `chapter-NN-topic/` 命名。`book.json` 是整本书的机器可读目录，LovStudio 官网会从 GitHub 的固定 commit 读取文章和 Prompt，不另外复制一份内容。

## 网站

- 系列阅读：<https://lovstudio.ai/research/agent-harness>
- Prompt Review：<https://lovstudio.ai/prompts?source=agent-harness-book>
- LovStudio：<https://lovstudio.ai>

## 版权

文章、编辑评论和原创图表按 [CC BY-NC-SA 4.0](LICENSE.md) 授权。Prompt 快照与上游源码仍归各自权利人所有，详见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

