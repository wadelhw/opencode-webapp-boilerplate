# AGENTS.md

## Development Principles

- Backend: FastAPI RESTful design
- Frontend: React functional components + TailwindCSS
- All changes must include tests
- Follow ADR process for architecture decisions

## API Standards

- Use Pydantic models
- Use dependency injection
- Return JSON only

## Frontend Standards

- Use functional components
- Use hooks only
- No inline styles (Tailwind only)

## Git Workflow

- feature/* branches
- PR required before merge
- CI must pass before merge

---

## AI Collaboration Guidelines

### Core Principles

- **描述清晰**: 给 AI 的指令要具体、明确
- **迭代优化**: 一次对话解决一个问题，逐步完善
- **验证优先**: 让 AI 先验证假设，再执行修改
- **保留上下文**: 使用 session 持续对话，避免重复解释

### Common Commands

| Command | Purpose |
|---------|---------|
| `/plan` | 进入规划模式，创建工作计划 |
| `/start-work` | 开始执行工作计划 |
| `/connect` | 连接 AI 服务提供商（设置 API key） |
| `/clear` | 清除当前会话上下文 |

### Workflow

1. **规划阶段**: 运行 `/plan`，描述需求，AI 会创建详细工作计划
2. **执行阶段**: 运行 `/start-work`，AI 按计划执行任务
3. **验证阶段**: 每个任务完成后 AI 会自动验证
4. **迭代**: 如有问题，继续对话修复

### Code Review Checklist

提交前检查：
- [ ] 代码符合项目规范
- [ ] 测试通过
- [ ] 无硬编码的敏感信息
- [ ] 文档已更新

