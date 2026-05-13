# AGENTS.md — 蒸馏器工作上下文

> 本文件为 Claude Code / OpenCode 提供蒸馏器项目的全局上下文与行为指令。

---

## 项目身份

你正在参与 **蒸馏器项目（Distiller）**，一个将古今中外名人资料蒸馏为高质量人物模拟 Skill 的自动化工具。

## 项目结构

```
distiller-skill/
├── AGENTS.md                  # ← 本文件
├── SKILL.md                   # 蒸馏器的主 skill 文件
├── README.md                  # 项目说明
├── templates/
│   └── celebrity-skill/
│       ├── SKILL.md           # 产出的人物 skill 模板
│       └── sources.md         # 产出的来源文件模板
├── distilled/                 # 已蒸馏的人物 skill 包（输出目录）
└── 蒸馏器项目-Distiller-企划书.md
```

## 当前状态

项目处于**验证阶段**，核心文件已全部创建，等待首次蒸馏测试。当前任务：

- [x] 企划书完成
- [x] SKILL.md（蒸馏器自身）
- [x] AGENTS.md（本文件）
- [x] README.md
- [x] templates/celebrity-skill/SKILL.md
- [x] templates/celebrity-skill/sources.md
- [ ] 首次蒸馏验证

## 行为约束

1. **消歧不可跳过**：任何情况下，遇到同名知名人物必须先确认再继续。
2. **来源不可伪造**：不得凭空编造 URL 或引用不存在的来源。所有来源须真实可访问。
3. **模板不可删减**：生成的 SKILL.md 必须包含全部 13 个模块（6 必选 + 7 可选）。
4. **编码必须正确**：所有文件 UTF-8 编码，路径无中文字符兼容性问题。
5. **质量必须自检**：每次蒸馏完成后，必须逐项核对校验清单。

## 技术约定

- Skill 格式：Superpowers 规范（YAML frontmatter + Markdown body）
- 输出目录：`distilled/{人物姓名}/`
- 文件名：英文或拼音（避免中文文件名在跨平台时的兼容性问题）
- 平台适配：优先使用 Claude Code / OpenCode 原生工具链

## 关键文件说明

| 文件 | 作用 | 谁读取 |
|------|------|--------|
| `SKILL.md` | 蒸馏器的主 skill 定义，包含完整蒸馏工作流 | Claude Code / OpenCode 加载 skill 时读取 |
| `AGENTS.md` | 项目全局上下文与行为约束 | Claude Code 启动时自动读取 |
| `templates/celebrity-skill/SKILL.md` | 人物模拟 skill 的标准模板 | 蒸馏器在生成阶段引用 |
| `templates/celebrity-skill/sources.md` | 来源文件的格式模板 | 蒸馏器在生成阶段引用 |

## 平台差异处理

| 功能 | Claude Code | OpenCode |
|------|-------------|----------|
| 联网搜索 | WebSearch 工具 | WebFetch / webfetch 工具 |
| Skill 加载 | `Skill` 工具 | `skill` 工具 |
| 文件操作 | Read / Write / Edit | read / write / edit |
| 任务列表 | TodoWrite | todowrite |
| Shell | Bash | bash |

## 下一步

完成所有核心文件后，选择一个名人（如"鲁迅"或"爱因斯坦"）进行首次蒸馏验证。
