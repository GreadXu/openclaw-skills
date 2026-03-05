# 部署指南

> OpenClaw Agent 部署完整指南

---

## 📋 目录

1. [本地部署](#本地部署)
2. [云部署](#云部署)
3. [飞书集成](#飞书集成)
4. [故障排查](#故障排查)

---

## 🖥️ 本地部署

### 前置条件

- Node.js >= 18
- OpenClaw 已安装
- 飞书应用凭证

### 步骤

```bash
# 1. 安装 OpenClaw
npm install -g openclaw

# 2. 配置飞书
openclaw config set feishu.appId YOUR_APP_ID
openclaw config set feishu.appSecret YOUR_APP_SECRET

# 3. 启动 Gateway
openclaw gateway start

# 4. 验证状态
openclaw status
```

---

## ☁️ 云部署

### 云服务商选择

| 服务商 | 推荐配置 | 预估成本 |
|--------|---------|---------|
| 阿里云 | ecs.t5.small | ~¥50/月 |
| 腾讯云 | s2.small | ~¥45/月 |
| AWS | t2.micro | ~$10/月 |

### 部署步骤（阿里云示例）

```bash
# 1. 创建 ECS 实例
# 选择 Ubuntu 22.04 LTS
# 开放端口：19000 (Gateway)

# 2. SSH 登录服务器
ssh root@YOUR_SERVER_IP

# 3. 安装 Node.js
curl -fsSL https://deb.nodesource.com/setup_20.x | bash -
apt-get install -y nodejs

# 4. 安装 OpenClaw
npm install -g openclaw

# 5. 配置飞书
openclaw config set feishu.appId YOUR_APP_ID
openclaw config set feishu.appSecret YOUR_APP_SECRET

# 6. 启动 Gateway (后台运行)
openclaw gateway start

# 7. 设置开机自启
openclaw gateway enable
```

### 安全配置

```bash
# 配置防火墙
ufw allow 22/tcp      # SSH
ufw allow 19000/tcp   # Gateway
ufw enable

# 配置 SSH 密钥登录
# 禁用密码登录
```

---

## 🤖 飞书集成

### 创建飞书应用

1. 访问 [飞书开放平台](https://open.feishu.cn/)
2. 创建企业自建应用
3. 配置机器人能力
4. 获取 App ID 和 App Secret

### 配置机器人

```yaml
# 在 OpenClaw 配置中
channels:
  feishu:
    appId: YOUR_APP_ID
    appSecret: YOUR_APP_SECRET
    dmPolicy: open  # 允许私聊
```

---

## 🔧 故障排查

### Gateway 无法启动

```bash
# 查看日志
openclaw gateway logs

# 检查端口占用
lsof -i :19000
```

### 飞书消息无法接收

1. 检查飞书应用配置
2. 验证回调 URL
3. 确认网络连通性

---

## 📞 获取帮助

- 文档：https://docs.openclaw.ai
- 社区：https://discord.gg/clawd
- 问题反馈：GitHub Issues
