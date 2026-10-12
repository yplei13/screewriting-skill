# 编剧导演 Skill（screenwriting）

中文电影、电视剧、网剧及短视频编剧助手。包含创作流程、人物塑造、对白方法和成稿自查，以及 9 份参考资料。

## 给 Agent 的安装说明

安装链接：https://github.com/yplei13/screewriting-skill/tree/main/screenwriting

可直接对支持 Skills 的 Agent 说：

> 请安装这个 skill：https://github.com/yplei13/screewriting-skill/tree/main/screenwriting 。请读取本仓库的 README，下载并安装整个 screenwriting 目录（包含 SKILL.md 和 references），完成后检查 9 份参考文件是否齐全。

### Codex

使用内置 `skill-installer`，将上述链接交给它。对应的安装命令是：

```text
python <skill-installer目录>/scripts/install-skill-from-github.py --url https://github.com/yplei13/screewriting-skill/tree/main/screenwriting
```

默认安装到 `$CODEX_HOME/skills/screenwriting`，未设置 `CODEX_HOME` 时安装到 `~/.codex/skills/screenwriting`。已有同名 skill 时先向用户说明冲突，不自动覆盖。安装完成后，在下一轮对话中使用 `$screenwriting`。

### Claude Code

下载或克隆本仓库，将完整 `screenwriting` 目录复制到 `~/.claude/skills/screenwriting`（用户级）或项目的 `.claude/skills/screenwriting`（项目级）。已有同名目录时不要自动覆盖。随后使用 `/screenwriting`。

### 其他支持 SKILL.md 的 Agent

将完整 `screenwriting` 目录复制到该 Agent 文档规定的 skill 目录。仅下载 `SKILL.md` 会丢失参考资料。不支持 Skills 的 Agent 需要先具备相应加载能力。

## 文件结构

```text
screenwriting/
├── SKILL.md
└── references/    # 9 份中文 Markdown 参考资料
```

该 skill 仅含 Markdown 文档，无需 API Key 或第三方运行依赖。所有参考文件均位于仓库内，使用相对路径引用。

原压缩包中的 `agent_created` 字段已移除，以兼容标准 skill 元数据；正文和参考资料保持原样。
