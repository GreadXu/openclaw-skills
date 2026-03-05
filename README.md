# OpenClaw Skills & Agent Registry 🌐

> 全能型 AI 助手的技能库与 Agent 注册表
> 用于 OpenClaw 和 Claude Code 的通用 Skills、模板和 Agent 管理

---

## 📁 仓库结构

```
openclaw-skills/
├── README.md                 # 本文件
├── agents/                   # Agent 注册表
│   ├── registry.md           # 所有 Agent 总览
│   ├── templates.md          # 模板 Agent 清单
│   ├── personal.md           # 个人 Agent 清单
│   └── inheritance-map.md    # 继承关系图
├── skills/                   # 技能库
│   ├── openclaw/             # OpenClaw 专用 Skills
│   ├── claude-code/          # Claude Code 专用 Skills
│   └── internet/             # 网络相关 Skills
├── templates/                # 模板库
│   ├── agent-config/         # Agent 配置模板
│   └── skill-template/       # Skill 创建模板
└── docs/                     # 文档
    ├── setup-guide.md        # 部署指南
    └── best-practices.md     # 最佳实践
```

---

## 🤖 Agent Registry

查看 [agents/registry.md](agents/registry.md) 获取完整的 Agent 清单，包括：

- **个人 Agent** - 你自己创建和使用的 Agent
- **模板 Agent** - 可复用的 Agent 模板
- **继承关系** - 模板 → 个人 Agent 的派生链
- **部署状态** - 本地 / 云服务器
- **飞书关联** - 绑定的飞书机器人

### 快速查找

| 查找方式 | 命令/位置 |
|---------|----------|
| 所有 Agent | `agents/registry.md` |
| 仅模板 | `agents/templates.md` |
| 仅个人 | `agents/personal.md` |
| 继承关系 | `agents/inheritance-map.md` |

---

## 🛠️ Skills 分类

### OpenClaw Skills
- Agent 管理工具
- 记忆/记录工具
- 飞书集成工具

### Claude Code Skills
- 项目初始化模板
- 代码规范
- 开发工作流

### Internet Skills
- 网络搜索工具
- API 集成
- Webhook 处理

---

## 📦 使用方式

### 1. 克隆仓库

```bash
git clone https://github.com/YOUR_USERNAME/openclaw-skills.git
cd openclaw-skills
```

### 2. 添加新 Agent

编辑 `agents/registry.md`，添加新记录。

### 3. 添加新 Skill

在对应的 `skills/` 子目录下创建 Skill 文件夹。

---

## 🚀 云部署

当前首个云部署 Agent：**Agent Nexus** (P0 优先级)

详见：[docs/setup-guide.md](docs/setup-guide.md)

---

## 📝 更新日志

- 2026-03-05: 初始版本，创建基础结构和 Agent Registry

---

## 📄 License

MIT
