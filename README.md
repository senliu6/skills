# Skills Repository

可复用的 AI Agent 技能集合，遵循 [Agent Skills](https://agentskills.io) 标准。

## 关于

这个仓库包含一系列模块化的技能（Skills），每个技能都是一个独立的文件夹，包含 `SKILL.md` 文件和相关资源。这些技能可以被 Claude 或其他支持 Agent Skills 标准的 AI 系统动态加载。

## 技能列表

每个技能都是自包含的，包含完整的指令、示例和资源文件。

## 使用方式

### 在 Claude Code 中使用

1. 将此仓库注册为插件市场
2. 浏览并安装需要的技能
3. 直接在对话中提及技能名称即可使用

### 在 API 中使用

参考 [Skills API 文档](https://docs.anthropic.com/en/docs/build-with-claude/skills)

## 创建新技能

每个技能需要：
1. 创建独立文件夹（使用 kebab-case 命名）
2. 添加 `SKILL.md` 文件，包含 YAML frontmatter 和指令
3. 可选：添加 `resources/` 文件夹存放支持文件

基本模板：

```markdown
---
name: skill-name
description: 清晰描述这个技能的功能和使用场景
---

# Skill Name

[技能的详细指令和说明]

## 使用示例

## 依赖项

## 注意事项
```

## 许可证

Apache 2.0
