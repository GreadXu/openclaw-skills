# Agent Registry - OpenClaw Agent 注册表

> 记录所有 Agent 的元数据、部署状态和飞书关联关系
> 最后更新：2026-03-05

---

## 📊 快速索引

### 按类型
- **个人 Agent:** 2
- **模板 Agent:** 1

### 按部署方式
- **本地:** 2
- **云服务器:** 0 (待部署)

### 按状态
- **活跃:** 2
- **开发中:** 0
- **休眠:** 0

---

## 📋 Agent 清单

### 1. 萤火 🔥 (main)

| 字段 | 值 |
|------|-----|
| **Agent ID** | main |
| **名称** | 萤火 (Firefly) |
| **类型** | 个人 Agent |
| **继承自** | - (原创) |
| **GitHub 仓库** | [GreadXu/agent-nexus](https://github.com/GreadXu/agent-nexus) |
| **功能领域** | 全能助手、Agent 管理、任务协调 |
| **Coding Plan** | - |
| **部署方式** | 本地 → **待迁移至云端** ☁️ |
| **云服务器信息** | (待配置) |
| **飞书机器人** | 当前会话机器人 |
| **模型** | bailian/qwen3.5-plus |
| **状态** | 活跃 ✅ |
| **创建日期** | 2026-03-02 |
| **最后更新** | 2026-03-05 |
| **备注** | 第一个 OpenClaw 全能助手，将首个上云部署 |

---

## 🎯 模板 Agent 清单

### 1. Claude Code Study Template

| 字段 | 值 |
|------|-----|
| **名称** | Claude Code Study Template |
| **仓库** | [code-firefly/claude-code-study-template](https://github.com/code-firefly/claude-code-study-template) |
| **类型** | 模板 Agent |
| **功能领域** | AI 学习、Claude Code 学习计划 |
| **派生 Agent** | Claude Code Study |
| **备注** | 官方学习计划模板 |

---

## 👤 个人 Agent 清单

### 1. Agent Nexus (main)

| 字段 | 值 |
|------|-----|
| **Agent ID** | main |
| **名称** | Agent Nexus |
| **类型** | 个人 Agent |
| **继承自** | - (原创) |
| **GitHub 仓库** | - |
| **功能领域** | 全能助手、Agent 管理、任务协调 |
| **Coding Plan** | - |
| **部署方式** | 本地 → **待迁移至云端** ☁️ |
| **云服务器信息** | (待配置) |
| **飞书机器人** | 当前会话机器人 |
| **模型** | bailian/qwen3.5-plus |
| **状态** | 活跃 ✅ |
| **创建日期** | 2026-03-02 |
| **最后更新** | 2026-03-05 |
| **备注** | 第一个 OpenClaw 全能助手，将首个上云部署 |

### 2. Claude Code Study

| 字段 | 值 |
|------|-----|
| **名称** | Claude Code Study |
| **仓库** | [GreadXu/claude-code-study](https://github.com/GreadXu/claude-code-study) |
| **模板仓库** | [code-firefly/claude-code-study-template](https://github.com/code-firefly/claude-code-study-template) |
| **类型** | 个人 Agent |
| **继承自** | code-firefly/claude-code-study-template |
| **功能领域** | AI 学习、代码开发 |
| **Coding Plan** | 智谱 Coding Plan |
| **部署方式** | 本地 |
| **飞书机器人** | (未绑定) |
| **模型** | (待确认) |
| **状态** | 活跃 ✅ |
| **备注** | 基于官方模板的个人学习用 Agent |

---

## 🔗 继承关系图

```
code-firefly/claude-code-study-template (模板)
    └── GreadXu/claude-code-study (个人 Agent)
```

---

## 🤖 飞书机器人关联表

| 飞书机器人 | 关联 Agent | 用途 | 状态 |
|-----------|-----------|------|------|
| 当前会话机器人 | Agent Nexus | 全能助手 | 活跃 |

---

## ☁️ 云部署计划

| Agent | 优先级 | 状态 | 计划日期 |
|-------|--------|------|---------|
| Agent Nexus | P0 | 准备中 | TBD |

---

## 📝 更新日志

- 2026-03-05: 创建初始注册表，记录 Agent Nexus 和模板/个人 Agent 信息
