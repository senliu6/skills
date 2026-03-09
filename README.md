# Skills Repository

可复用的 AI Agent 技能集合，遵循 [Agent Skills](https://agentskills.io) 标准。

## 关于

这个仓库包含一系列模块化的技能（Skills），每个技能都是一个独立的文件夹，包含 `SKILL.md` 文件和相关资源。这些技能可以被 Claude 或其他支持 Agent Skills 标准的 AI 系统动态加载。

## 技能列表

每个技能都是自包含的，包含完整的指令、示例和资源文件。

## 使用方式

### 方式 1: Git Submodule（推荐）

在你的项目中添加此技能库作为子模块：

```bash
# 添加子模块
git submodule add https://github.com/senliu6/skills.git .kiro/skills

# 或添加到自定义路径
git submodule add https://github.com/senliu6/skills.git skills

# 更新子模块
git submodule update --init --recursive
```

### 方式 2: 直接克隆

```bash
# 克隆到项目目录
cd your-project
git clone https://github.com/senliu6/skills.git .kiro/skills
```

### 方式 3: Steering 文件引用

在你的项目 `.kiro/steering/` 目录中创建引用文件：

```markdown
---
name: external-skills
description: 引用外部技能库
inclusion: always
---

# 外部技能引用

使用以下技能时，参考：https://github.com/senliu6/skills

- api-design: API 设计规范
- code-review: 代码审查标准
- test-generator: 测试生成
- refactor-assistant: 重构建议
```

### 方式 4: 在 Claude Code 中使用

如果你的技能库注册为插件：

1. 打开 Claude Code
2. 运行命令安装插件
3. 在对话中直接提及技能名称

### 方式 5: 通过 API 使用

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
