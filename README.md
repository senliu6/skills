# Skills Repository

可复用的 AI Agent 技能集合，遵循 [Agent Skills](https://agentskills.io) 标准。

## 快速开始

在 Claude Code 中直接使用 Git 链接导入：

```bash
kiro plugins add https://github.com/senliu6/skills.git
```

或在对话中说：
```
请添加技能库：https://github.com/senliu6/skills.git
```

## 关于

这个仓库包含一系列模块化的技能（Skills），每个技能都是一个独立的文件夹，包含 `SKILL.md` 文件和相关资源。这些技能可以被 Claude 或其他支持 Agent Skills 标准的 AI 系统动态加载。

## 技能列表

- **api-design** - RESTful API 设计规范
- **code-review** - 系统化代码审查
- **test-generator** - 自动生成测试代码
- **refactor-assistant** - 代码重构建议

详细使用方法见 [USAGE.md](./USAGE.md)

## 贡献

欢迎贡献新技能！详见 [CONTRIBUTING.md](./CONTRIBUTING.md)

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

### 方式 4: 在 Claude Code 中通过 Git 链接导入

直接使用 Git 链接注册技能库：

```bash
# 在 Claude Code 中运行
kiro plugins add https://github.com/senliu6/skills.git

# 或者通过命令面板
# 1. 打开命令面板 (Cmd/Ctrl + Shift + P)
# 2. 搜索 "Add Plugin from Git"
# 3. 输入: https://github.com/senliu6/skills.git
```

然后在对话中直接使用技能：
```
使用 api-design 技能帮我设计用户管理 API
使用 code-review 技能审查这段代码
```

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
