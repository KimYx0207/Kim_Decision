<div align="center">

<h1 style="font-size: 4em; font-weight: 900; margin-bottom: 0.2em; letter-spacing: 0.1em;">Kim - Service</h1>
<p style="font-size: 1.2em; color: #7c3aed; font-weight: 600; margin-top: 0;">工具集</p>

<p>
  <a href="README.md">English</a> |
  <a href="README.zh-CN.md">简体中文</a>
</p>

<p>
  <img alt="Runtime" src="https://img.shields.io/badge/runtime-Claude%20Code%20%7C%20Codex-111827"/>
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green"/>
</p>

</div>

## 简介

**Kim - Service** 是一套面向 AI 编码助手的工具集，为 Claude Code 和 Codex 提供可复用的 Hooks 和 Skills。

### 一句话总结

> **把生产级工具封装成即插即用的组件，让 AI 编码助手如虎添翼。**

这不是简单的脚本集合——它是经过实战验证的生产力工具包，开箱即用。

## 快速开始

```bash
# 克隆到本地
git clone https://github.com/KimYx0207/Kim_Service.git
cd Kim_Service

# 使用 Claude Code 或 Codex
# 直接将对应目录复制到项目根目录即可
```

---

## 目录结构

```
Kim_Service/
├── Hooks/
│   └── Hook_Prompt/              # 提示词自动优化 Hook
│       ├── .claude/
│       │   ├── hooks/            # Hook 脚本
│       │   ├── prompt-optimizer-meta.md
│       │   └── settings.json
│       └── README.md
├── Skills/
│   ├── Agent_Teams_Playbook/    # Agent 团队编排手册
│   │   └── agent-teams-playbook/
│   ├── Claude_Memory_3layer/    # 三层记忆系统
│   │   ├── hooks/               # 记忆 Hook
│   │   └── commands/            # 记忆命令
│   ├── Find_Skill/              # 技能发现工具
│   └── Kim_Decision/            # 决策框架
├── README.md
└── LICENSE
```

## 组件介绍

### Hooks

| 名称 | 运行时 | 功能 |
|------|--------|------|
| Hook_Prompt | Claude Code / Codex | 将模糊需求自动优化为专业提示词，集成谷歌提示词工程最佳实践 |

### Skills

| 名称 | 触发词 | 功能 | 运行时 |
|------|--------|------|--------|
| agent-teams-playbook | 多agent、agent协作、agent编排 | 跨平台 Agent Teams 编排手册 | Claude Code / Codex |
| claude-memory-3layer | 三层记忆、跨会话记忆 | 三层记忆系统，跨会话持久化知识 | Claude Code |
| find-skill | 找技能、发现技能 | 技能发现与安装 | Claude Code / Codex |
| Kim_Decision | 决策、选择 | 决策框架与示例 | 全平台 |

## 架构：工具链 + 工作流

Kim_Service 的组件可以独立使用，也可以组合成完整的工作流：

```mermaid
flowchart LR
    H[Hook 拦截] --> P[Prompt 优化]
    P --> S[Skill 执行]
    S --> M[记忆保存]
    M --> R[结果返回]

    style H fill:#fbbf24,color:#000
    style P fill:#34d399,color:#000
    style S fill:#60a5fa,color:#000
    style M fill:#a78bfa,color:#fff
    style R fill:#f87171,color:#fff
```

### Hook 层

在 Claude Code 中，Hooks 实现自动化：

- **Prompt 优化**：用户输入自动优化为专业提示词
- **危险命令拦截**：防止误操作
- **格式化**：编辑后自动格式化
- **记忆保存**：会话结束自动保存上下文

### Skill 层

Skills 提供专业能力：

- **Agent Teams**：多 agent 协作编排
- **Memory**：三层跨会话记忆
- **Decision**：决策框架

---

## 安装使用

### 在当前项目使用（Claude Code）

将 `.claude/` 目录复制到你的项目根目录：

```bash
# Unix/macOS
cp -r Hooks/Hook_Prompt/.claude /your-project/

# Windows
xcopy /E /I Hooks\Hook_Prompt\.claude your-project\
```

### 全局安装

```bash
# Claude Code
mkdir -p ~/.claude/hooks
cp -r Hooks/Hook_Prompt/.claude/hooks/* ~/.claude/hooks/
cp Hooks/Hook_Prompt/.claude/prompt-optimizer-meta.md ~/.claude/

# Codex
mkdir -p ~/.codex/hooks
cp -r Hooks/Hook_Prompt/.claude/hooks/* ~/.codex/hooks/
```

### 安装 Skills

```bash
# Claude Code
claude skill install KimYx0207/agent-teams-playbook

# 或使用 npx
npx --yes github:KimYx0207/Kim_Service/skills/agent-teams-playbook
```

---

## 跨平台支持

| 平台 | Hooks | Skills | 备注 |
|------|-------|--------|------|
| **Claude Code** | ✅ | ✅ | 主编辑运行时 |
| **Codex** | ✅ | ✅ | hooks.json 支持 |

---

## 运维命令速查

| 命令 | 作用 |
|------|------|
| Hook_Prompt 测试 | `node test-hook.js` |
| 验证 Hook 配置 | 检查 `.claude/settings.json` |

---

## 许可

本项目基于 MIT 协议开源，详见 [LICENSE](LICENSE) 文件。

---

## 联系方式

GitHub <a href="https://github.com/KimYx0207">KimYx0207</a> |
X <a href="https://x.com/KimYx0207">@KimYx0207</a> |
官网 <a href="https://www.aiking.dev/">aiking.dev</a>

---

## License

本项目采用 [MIT License](LICENSE)。