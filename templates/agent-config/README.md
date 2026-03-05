# Agent 配置模板

> 创建新 Agent 的标准配置模板

---

## 📁 必需文件

```
agent-name/
├── IDENTITY.md           # Agent 身份定义
├── SOUL.md              # Agent 行为和风格
├── config.yaml          # 配置文件
└── README.md            # 使用说明
```

---

## 📝 IDENTITY.md 模板

```markdown
# IDENTITY.md - Who Am I?

- **Name:** Your Agent Name
- **Creature:** AI Assistant / Specialist
- **Vibe:** Professional / Casual / etc.
- **Emoji:** 🤖
- **Avatar:** (optional)

---

## Role
描述 Agent 的角色和职责。

## Mission
描述 Agent 的使命和目标。
```

---

## 📝 config.yaml 模板

```yaml
agent:
  name: your-agent-name
  model: bailian/qwen3.5-plus
  workspace: ~/.openclaw/workspace/your-agent
  
skills:
  - skill-name-1
  - skill-name-2

deployment:
  type: local  # 或 cloud
  cloud:
    provider: aliyun  # 如果使用云部署
    instance: ecs.t5.small
```

---

## 🚀 创建步骤

1. 复制此模板文件夹
2. 重命名为你的 Agent 名称
3. 编辑配置文件
4. 在 `agents/registry.md` 中注册
