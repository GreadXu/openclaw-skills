# Skills 库

> OpenClaw 和 Claude Code 的通用技能库

---

## 📁 目录结构

```
skills/
├── openclaw/             # OpenClaw 专用 Skills
│   ├── agent-manager/    # Agent 管理相关
│   └── memory-tools/     # 记忆/记录工具
├── claude-code/          # Claude Code 专用 Skills
│   ├── project-setup/    # 项目初始化
│   └── coding-templates/ # 代码模板
└── internet/             # 网络相关 Skills
    ├── web-search/       # 搜索工具
    ├── api-integrations/ # API 集成
    └── webhooks/         # Webhook 处理
```

---

## 🛠️ Skill 分类

### OpenClaw Skills
用于 OpenClaw 平台的专用技能，包括：
- Agent 生命周期管理
- 飞书集成
- 记忆系统
- 任务调度

### Claude Code Skills
用于 Claude Code 的专用技能，包括：
- 项目初始化模板
- 代码规范检查
- 开发工作流自动化

### Internet Skills
网络相关技能，包括：
- 多引擎搜索
- API 集成工具
- Webhook 处理器
- 数据抓取

---

## 📦 如何添加新 Skill

1. 在对应分类下创建新文件夹
2. 添加 `SKILL.md` 描述文件
3. 添加必要的脚本和资源
4. 在本目录 README 中注册

---

## 🔗 相关文档

- [Skill 创建模板](../templates/skill-template/)
- [最佳实践](../docs/best-practices.md)
