# spec-skills

An agent skill for writing a [spex](https://www.npmjs.com/package/@sublang/spex) `specs/` tree for an existing codebase.

| Skill | What it does |
| --- | --- |
| [`spec-extraction`](skills/spec-extraction/SKILL.md) | Writes a lawful, evidence-backed `specs/` tree for a project that has none, describing the code as it is. Resumable: it keeps its plan and evidence ledger in the target project's `.specs-extraction/`. |

## Install

With the [skills CLI](https://skills.sh/):

```sh
npx skills add kagami-l/spec-skills --skill spec-extraction
```

Add `-g` to install for your user instead of the current project, `-a claude-code` to pick the agent, or `--list` to see what the repo offers.

## Requirements

- Node.js, for `npx -y @sublang/spex@<version>`; the version is pinned once in the skill's `SKILL.md`.
- An agent host with subagents, such as Claude Code, for the fresh-context reviewers; without them the human opens those contexts.

## Use

In the project that needs specs, start a session and invoke `/spec-extraction`.
The run stops at the human gates (plan review, calibration, final review); invoke it again to continue from the next unchecked item in `.specs-extraction/plan.md`.

## License

[Apache-2.0](LICENSE)

---

# spec-skills（中文）

为已有代码库编写符合 [spex](https://www.npmjs.com/package/@sublang/spex) 规范的 `specs/` 的 agent skill。

| Skill | 作用 |
| --- | --- |
| `spec-extraction` | 为没有 specs 的项目按代码现状写出合法、有证据支撑的 `specs/` 树；计划与证据台账放在目标项目的 `.specs-extraction/`，可中断续跑。 |

## 安装

```sh
npx skills add kagami-l/spec-skills --skill spec-extraction
```

`-g` 装到用户级，`-a claude-code` 指定 agent，`--list` 列出可装的 skill。

## 依赖

- Node.js，用于 `npx -y @sublang/spex@<版本>`，版本只在 skill 的 `SKILL.md` 声明一次。
- 支持子代理的 agent 宿主（如 Claude Code），用于新鲜上下文的 reviewer；没有时由人自己开这些上下文。

## 使用

在需要 specs 的项目里开会话，输入 `/spec-extraction`。run 会停在人工关卡（计划审阅、校准、终审）；再次输入同一命令，从 `.specs-extraction/plan.md` 的下一个未勾选项继续。

## 许可证

[Apache-2.0](LICENSE)
