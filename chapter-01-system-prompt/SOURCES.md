# Chapter 01 来源与口径

## 文章基准

| Harness | 版本 | 本章审阅对象 |
| --- | --- | --- |
| Codex | `codex-cli 0.149.1` | `gpt-5.6-sol` 模型目录下发的 `model_messages.instructions_template` |
| Claude Code | 当前 CLI `2.1.233` + 历史 `2.1.88` | 当前官方追加/替换接口，以及 2026-03-31 source map 快照里的 `getSystemPrompt()` 组装链 |
| Pi | `v0.73.1` | `packages/coding-agent/src/core/system-prompt.ts` 中的 `buildSystemPrompt()` |
| DSH | `dsh-v0.1.0-rc.8` | System Prompt registry 与 `text-turn/system-prompt.expected.md` 渲染快照 |

## 为什么四个文件不长得一样

因为四家并不共享同一种 System Prompt 设计：

- Codex 有一份可直接保存的模型级 base template。
- Claude Code 的默认文本由多个静态和动态 section 拼出；历史快照最可审阅的对象是 builder 本身。
- Pi 把默认骨架、工具、项目文件和 Skills 放在一个公开函数里组装。
- DSH 由插件各自贡献 section，所以本章保存一个官方测试用的已渲染快照。

因此，这个目录提供的是“各家最接近真实的可审阅对象”，不是为了表面对称而人造四份静态 Prompt。

