# talklikehumans

[![license](https://img.shields.io/github/license/5havv/talklikehumans)](./LICENSE)

[English](https://github.com/5havv/talklikehumans/blob/main/README.en.md) | **中文**

让大模型 agent 说人话：一条 rules，禁掉一些黑话。

## 简单说明

大模型很爱用偏门术语，对于人来说很难理解。

本项目只有一个 `README.md`：这条 rule 的说明，加上可以直接复制的原文。没有代码，不需要安装。

## 如何使用

把下面整段文字复制到你的 agent 里。粘进对话让它写进 rules 就行，也可以自己放进 `CLAUDE.md`、`AGENTS.md`、`.cursor/rules/` 或系统提示词：

```text
请添加rules：不要用下列词充当「看起来专业」的标签或动词：

- 门禁
- 闭环
- 收口
- 闸门
- 扳机
- 准入
- 种子
- 管控面
```

写进 rules 之后不用重启，新开的会话就会生效：agent 一旦准备用这些词，就会换成更直白的表达。

## 一点补充

- 这七个词只是最常见的样本。你自己的黑名单可以照同样的格式追加在后面。
- 规则管的是「不要拿它们当标签或动词」，不是彻底禁用：如果某个词在你的项目里是真实存在的专有名词（比如代码里真有个叫 `gate` 的模块），照旧用它本来的名字。

## 许可证

[MIT](./LICENSE)
