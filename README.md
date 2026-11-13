# Codex 方案交接

用 Codex 只做方案分析，写成决策完整的计划文件；你审阅后再交给 Grok 或其他 agent，在本地仓库里执行。适合较大的功能或重构，小修补不必走这套。

Codex 和执行方都应在本地仓库里工作，不要把业务代码上传到别处。

## 怎么用

1. 确认方案文件路径。没有现成约定时，建议用 `docs/plans/YYYY-MM-DD-<短名>.md`；仓库里若已有文档目录习惯，跟已有习惯走。把该路径代入 `SKILL.md` 里的 `<方案文件路径>`。
2. 把「交给 Codex」那段提示词贴给 Codex，填上你的需求。它只应写入那一份方案文件。
3. 你先审阅方案，改掉不同意的地方。
4. 把「交给执行方」那段提示词，连同方案文件，交给 Grok 或其他执行 agent。
5. 可选：把 diff 交回 Codex，用「只读审查」那段提示词做审查，比较省额度。

完整提示词见 [SKILL.md](./SKILL.md)。

## 安装

- **Cursor**：把 `SKILL.md` 复制到项目里的 `.cursor/skills/codex-plan-handoff/SKILL.md`，或放到你的用户 skill 目录。
- **Grok Bot**：把 `SKILL.md` 复制进 skill 库后，可用 `/` 或 `@` 调出「Codex 方案交接」。
