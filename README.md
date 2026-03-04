# opencode-webapp-boilerplate

使用 opencode + oh-my-opencode 进行 AI 辅助开发的脚手架模板。

## 特性

- 🚀 开箱即用的 opencode 配置
- 🤖 预配置的 AI Agents（Sisyphus, Oracle, Prometheus 等）
- 📋 标准化的开发规范（AGENTS.md）
- 🔧 Web App 开发最佳实践

## 快速开始

### 1. 克隆脚手架

```bash
git clone https://github.com/wadelhw/opencode-webapp-boilerplate.git my-project
cd my-project
rm -rf .git
git init
```

### 2. 安装 opencode

```bash
npm install -g @anthropics/claude-code
# 或
bun install -g @anthropics/claude-code
```

### 3. 连接 AI 服务

```bash
opencode
# 在 TUI 中运行：/connect
```

### 4. 开始开发

```bash
# 在 opencode TUI 中:
/plan 创建一个用户管理 API
/start-work
```

## 配置文件

| 文件 | 说明 |
|------|------|
| `opencode.json` | opencode 核心配置（模型、MCP、权限） |
| `oh-my-opencode.json` | oh-my-opencode agent 配置 |
| `AGENTS.md` | 开发规范和 AI 协作指南 |

## 开发规范

详见 [AGENTS.md](./AGENTS.md)

## 相关链接

- [opencode](https://opencode.ai)
- [oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode)
