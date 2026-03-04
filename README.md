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

### 2. 连接 AI 服务

```bash
opencode
# 在 TUI 中运行：/connect
# 选择你的 AI 服务提供商并配置 API Key
```

### 3. 让 AI 读取项目需求

在 opencode TUI 中，让 AI 读取 README：

```
请阅读 README.md，了解项目需求并帮我生成定制化的 opencode 配置
```

AI 会：
- 分析你的项目需求
- 调整 `opencode.json` 中的模型配置
- 配置合适的 MCP 服务器
- 设置项目特定的开发规范

### 4. 重启 opencode

退出并重新启动 opencode，让新配置生效：

```bash
# 按 Ctrl+C 或输入 /exit 退出
opencode  # 重新启动
```

### 5. 开始开发

现在可以开始正式开发了：

```
/plan 创建一个用户管理 API，包含注册、登录、查询功能
/start-work
```

## 工作流程说明

```
┌─────────────────────────────────────────────────────────────┐
│                    完整开发流程                              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. Clone     ──►  2. Connect    ──►  3. Configure        │
│  获取脚手架        配置 AI 服务       AI 读取需求           │
│                                                             │
│       │                                                    │
│       ▼                                                    │
│                                                             │
│  4. Restart   ──►  5. Develop                              │
│  重启生效            开始开发                               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 为什么需要「AI 读取需求」这一步？

脚手架提供的是**通用配置**，每个项目可能有不同需求：

| 需求类型 | 示例 |
|---------|------|
| **技术栈** | React + FastAPI / Vue + Node.js / Next.js 全栈 |
| **AI 模型** | Claude / GPT-5 / 国产模型（智谱、百炼） |
| **MCP 服务** | 数据库连接 / 外部 API / 文档搜索 |
| **开发规范** | 代码风格 / 测试要求 / Git 规范 |

通过让 AI 读取你的项目需求，可以：
- ✅ 自动调整模型配置（如使用国产模型）
- ✅ 配置项目需要的 MCP 服务器
- ✅ 设置 `instructions` 指向你的规范文件
- ✅ 调整权限和工具配置

## 配置文件

| 文件 | 说明 | 可定制项 |
|------|------|---------|
| `opencode.json` | opencode 核心配置 | 模型、MCP、权限、指令 |
| `oh-my-opencode.json` | oh-my-opencode agent 配置 | Agent 模型、并发数 |
| `AGENTS.md` | 开发规范和 AI 协作指南 | 项目规范、代码风格 |

### 配置参考

完整配置选项请参考官方文档：
- [opencode 配置文档](https://opencode.ai/docs/zh-cn/config/)
- [oh-my-opencode 文档](https://github.com/code-yeongyu/oh-my-opencode)

## 常见定制场景

### 场景 1：使用国产 AI 模型

```
请帮我配置使用智谱 GLM-5 模型，并配置百炼作为备用
```

### 场景 2：添加数据库 MCP

```
请帮我配置 PostgreSQL MCP 服务器，连接字符串是 postgresql://...
```

### 场景 3：设置项目规范

```
请将 `docs/coding-standards.md` 添加到 instructions，让 AI 遵循我们的代码规范
```

## 开发规范

详见 [AGENTS.md](./AGENTS.md)

## 相关链接

- [opencode 官网](https://opencode.ai)
- [opencode 配置文档](https://opencode.ai/docs/zh-cn/config/)
- [oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode)
