# talklikehumans

[![license](https://img.shields.io/github/license/5havv/talklikehumans)](./LICENSE)

[中文](https://github.com/5havv/talklikehumans/blob/main/README.md) | **English**

Make your LLM agent talk like a human: one rule that bans jargon labels such as "gatekeeping", "closed loop" and "control plane".

## What this is

LLM agents love reaching for words like 门禁, 闭环 or 管控面 as labels or verbs, because they sound professional. They add no meaning — they just wrap a sentence anyone could follow in slide-deck language. With this rule in place, the agent skips them and says the concrete thing instead.

This project is a single `README.md`: the rule, plus the text you can copy straight into your agent. No code, nothing to install.

## How to use

Copy the whole block below into your agent. Paste it into the chat and ask it to save it as a rule, or add it by hand to `CLAUDE.md`, `AGENTS.md`, `.cursor/rules/`, or your system prompt:

```text
Please add a rule: do not use the following words as labels or verbs just to sound "professional" (the original Chinese terms are in parentheses):

- gating / access control (门禁)
- closed loop (闭环)
- closing out / sealing off (收口)
- gate / floodgate (闸门)
- admission / entry control (准入)
- seed / seeding (种子)
- control plane (管控面)
```

Once the rule is saved, no restart is needed — new sessions pick it up. The moment the agent is about to reach for one of these words, it will phrase things plainly instead.

## Notes

- The list was written in Chinese, so the originals are kept in parentheses; that way the same rule also holds for an agent writing in Chinese.
- Those seven words are just the common offenders. Append your own in the same format.
- The rule bans them as labels or verbs, not outright: if a word is a real identifier in your project (say, a module actually named `gate`), keep calling it what it is.

## License

[MIT](./LICENSE)
