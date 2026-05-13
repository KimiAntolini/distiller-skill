# 蒸馏器（Distiller）

> 一键蒸馏古今中外名人，生成高质量 AI 人物模拟 Skill。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **📖 English**：[README.en.md](./README.en.md)

## 这是什么？

蒸馏器是一个 AI 驱动的自动化工具。你输入一个名人姓名，它联网搜索全网公开资料，深度蒸馏整合，最终生成一个可直接使用的人物模拟 Skill 包 —— 让 AI 能够逼真地模拟该名人进行对话和思考。

## 快速开始

### 方式一：Skill.sh 一键安装

```bash
skill install distiller
```

### 方式二：GitHub 克隆

```bash
git clone https://github.com/anomalyco/distiller-skill.git
```

将 `distiller-skill` 目录放入你的 skills 目录即可。

### 使用

在 Claude Code 或 OpenCode 中：

```
蒸馏 鲁迅
```

或：

```
生成爱因斯坦的 skill
```

蒸馏器会自动搜索、消歧、采集资料、整合并生成完整的 Skill 包。

> **💡 提示**：与 [superpowers](https://github.com/obra/superpowers) 和 [skill-creator](https://skill.sh) 两个 skill 配合使用，蒸馏效果更佳。superpowers 提供规范的工作流体系，skill-creator 帮助你打磨、调试和优化生成的 skill。

## 输出物

每次蒸馏生成一个独立文件夹：

```
distilled/{人物姓名}/
├── SKILL.md       # 人物模拟 skill（13 个模块）
└── sources.md     # 所有参考资料来源
```

### SKILL.md 包含的模块

**必选（6）：**
1. 人物性格
2. 人物语言风格
3. 人物行事风格
4. 人物著作
5. 人物历史/生平
6. 人物思想分析

**可选（7）：**
7. 人物关系网络
8. 轶事典故
9. 后人评价
10. 思想流派对照
11. 代表性言论摘录
12. 模拟对话示例
13. 补充资料索引

## 支持的人物范围

- ✅ 古代中国名人（先秦至清）
- ✅ 近现代中国名人（1840–1949）
- ✅ 当代中国名人（1949 至今）
- ✅ 外国名人（所有地区/时代）
- 🔮 普适蒸馏器（V2.0 规划中）—— 支持蒸馏任意人的私有数据

## 兼容平台

| 平台 | 状态 |
|------|------|
| Claude Code | ✅ 原生支持 |
| OpenCode | ✅ 原生支持 |
| Codex | ⚠️ 需适配 |
| Copilot CLI | ⚠️ 需适配 |
| Gemini CLI | ⚠️ 需适配 |

## 项目结构

```
distiller-skill/
├── SKILL.md                           # 蒸馏器主 skill 文件
├── AGENTS.md                          # 项目上下文
├── README.md                          # 本文件
├── templates/celebrity-skill/
│   ├── SKILL.md                       # 人物 skill 模板
│   └── sources.md                     # 来源文件模板
├── distilled/                         # 输出目录
├── 蒸馏器项目-Distiller-企划书.md      # 完整企划文档
└── LICENSE
```

## 贡献

欢迎提交 Issue 和 PR。请先阅读 [蒸馏器项目-Distiller-企划书.md](./蒸馏器项目-Distiller-企划书.md) 了解项目全貌。

## 许可

MIT License
