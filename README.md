# GRE Issue Writing & Expression Training

一个面向 GRE Issue 写作的 Codex skill，短练习为主，适用于写作能力恢复训练
以锻炼问题分析、逻辑构思、英文遣词能力为主

## 功能

- 训练 GRE 写作中高频、可迁移的词汇搭配
- 练习 Issue 立场、理由、因果链和反方回应
- 训练论点从中文思考到英文表达的转换
- 检查词性、单复数、可数性和介词使用
- 区分语法错误、搭配错误、不自然表达和风格优化
- 减少中文直译和中式英语
- 训练近义词的语义范围与正式程度
- 根据学习者表现动态调整练习难度
- 在当前对话中归纳反复出现的错误类型

## 训练流程

每轮只推进一个阶段：

1. **Issue Argument Generation**：分析一道英文 GRE Issue 题目，形成立场、理由、因果链和反方回应。
2. **English Expression Translation**：将本轮论点中的 3–5 个中文句子翻译成英文。
3. **Collocation Recall**：把本轮话题和薄弱点中的 5 个中文搭配译成英文。
4. **Sentence Transfer**：将重点搭配应用到新的 GRE Issue 语境。
5. **Error Archive**：总结严重问题、重复错误、重点表达和下一轮训练方向。

默认目标是达到 GRE 3.5–4.0 写作所需的清晰论证、准确表达和自然搭配，而不是堆砌生僻词或高级词汇。

## 使用方式

安装后可以直接对 Codex 说：

```text
开始 GRE Issue 写作训练
```

或明确指定 skill：

```text
使用 gre-collocation-coach 开始训练
```

启动时会从 Issue Argument Generation 开始。之后直接提交答案，skill 会根据当前对话状态进入相应阶段。

## 安装

将整个 `gre-collocation-coach` 文件夹放入 Codex 的 skills 目录。README 不包含机器相关的绝对路径；安装后的相对目录结构如下：

```text
skills/gre-collocation-coach/
```

目录结构如下：

```text
gre-collocation-coach/
├── SKILL.md
├── README.md
└── agents/
    └── openai.yaml
```

## 设计原则

- 不把本来正确的表达强行改成更复杂的表达。
- 明确区分错误、较不自然的表达和可选的风格优化。
- 优先提供少量最值得记住的自然表达，而不是罗列大量同义词。
- 解释错误背后的规律，帮助学习者迁移到其他题目。
- 论点生成默认约 4–5 分钟，英文翻译约 5 分钟，搭配回忆约 3 分钟；这些是用户侧计时目标，不代表 skill 会精确测量时间。

## 状态说明

错误模式会在当前对话中持续追踪。除非外部系统实际保存了学习记录，否则 skill 不会声称能够跨对话记住学习者的表现。

