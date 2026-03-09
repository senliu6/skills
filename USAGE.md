# 使用指南

## 快速开始

### 在 Claude Code 中使用（推荐）

最简单的方式是直接通过 Git 链接导入：

```bash
kiro plugins add https://github.com/senliu6/skills.git
```

或者在 Claude Code 对话中直接说：

```
请添加这个技能库：https://github.com/senliu6/skills.git
```

### 在其他项目中使用

#### 1. 作为 Git Submodule

```bash
# 在你的项目根目录
git submodule add https://github.com/senliu6/skills.git .kiro/skills

# 初始化和更新
git submodule update --init --recursive

# 后续更新技能库
cd .kiro/skills
git pull origin main
```

#### 2. 直接克隆

```bash
cd your-project
git clone https://github.com/senliu6/skills.git .kiro/skills

# 更新时
cd .kiro/skills
git pull
```

#### 3. 通过 Steering 引用

在 `.kiro/steering/skills-reference.md` 中：

```markdown
---
name: skills-reference
description: 引用外部技能库
inclusion: always
---

# 技能库引用

本项目使用以下技能：https://github.com/senliu6/skills

可用技能：
- api-design: RESTful API 设计
- code-review: 代码审查
- test-generator: 测试生成
- refactor-assistant: 重构建议
```

## 使用示例

### 在对话中使用技能

```
# 使用 API 设计技能
使用 api-design 技能帮我设计一个博客系统的 API

# 使用代码审查技能
使用 code-review 技能审查 src/utils/helper.js

# 使用测试生成技能
使用 test-generator 为 UserService 类生成测试

# 使用重构助手
使用 refactor-assistant 分析 components/Dashboard.jsx
```

### 组合使用多个技能

```
1. 先用 api-design 设计 API
2. 再用 code-review 审查实现
3. 最后用 test-generator 生成测试
```

## 配置选项

### 选择性加载技能

如果只需要部分技能，可以：

```bash
# 只克隆需要的技能文件夹
git clone --depth 1 --filter=blob:none --sparse https://github.com/senliu6/skills.git
cd skills
git sparse-checkout set api-design code-review
```

### 自定义技能路径

```bash
# 安装到自定义位置
git submodule add https://github.com/senliu6/skills.git custom/path/skills
```

## 更新技能库

```bash
# 如果使用 submodule
git submodule update --remote .kiro/skills

# 如果直接克隆
cd .kiro/skills && git pull
```

## 贡献新技能

欢迎贡献新技能！

1. Fork 此仓库
2. 基于 `template-skill` 创建新技能
3. 提交 Pull Request

详见 [CONTRIBUTING.md](./CONTRIBUTING.md)
