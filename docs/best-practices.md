# 最佳实践

> OpenClaw Agent 开发和管理的最佳实践

---

## 📝 Agent 设计原则

### 1. 专注单一职责

每个 Agent 应该有明确的功能领域，避免全能但平庸。

**好的例子：**
- 📅 日历管理 Agent
- 📧 邮件处理 Agent
- 💻 代码审查 Agent

**避免：**
- 试图处理所有任务的"万能"Agent

### 2. 清晰的继承关系

使用模板创建新 Agent 时，明确记录继承关系：

```
模板 Agent → 个人 Agent
    ↓
记录在 inheritance-map.md
```

### 3. 统一的命名规范

```
格式：<用途>-<类型>-agent
示例：
- study-claude-code-agent
- manage-calendar-agent
- monitor-server-agent
```

---

## 🗂️ 文件组织

### Registry 更新频率

| 事件 | 更新要求 |
|------|---------|
| 创建新 Agent | 立即更新 |
| 部署方式变更 | 立即更新 |
| 飞书绑定变更 | 立即更新 |
| 状态变更 | 24 小时内更新 |

### Skills 管理

- 每个 Skill 独立文件夹
- 必须包含 `SKILL.md` 描述
- 版本化发布（使用 Git 标签）

---

## 🔒 安全实践

### 凭证管理

- ❌ 不要将 API Key 提交到 Git
- ✅ 使用环境变量或加密存储
- ✅ 定期轮换凭证

### 云部署安全

- 使用 SSH 密钥登录
- 配置防火墙规则
- 启用安全组
- 定期更新系统

---

## 📊 监控与日志

### 推荐监控指标

- Agent 响应时间
- 消息处理成功率
- 资源使用率（云部署）

### 日志保留

- 本地：保留最近 7 天
- 云端：保留最近 30 天

---

## 🔄 版本控制

### Git 工作流

```bash
# 开发新功能
git checkout -b feature/new-skill

# 提交更改
git add .
git commit -m "feat: add new skill for X"

# 推送到远程
git push origin feature/new-skill
```

### 提交信息规范

```
feat: 新功能
fix: 修复问题
docs: 文档更新
style: 格式调整
refactor: 重构
test: 测试相关
chore: 其他
```

---

## 📚 学习资源

- [OpenClaw 官方文档](https://docs.openclaw.ai)
- [Claude Code 文档](https://docs.anthropic.com/claude-code)
- [飞书开放平台](https://open.feishu.cn/)
