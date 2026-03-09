# 贡献指南

感谢你对这个技能库的兴趣！

## 如何贡献新技能

### 1. 准备工作

```bash
# Fork 并克隆仓库
git clone https://github.com/YOUR_USERNAME/skills.git
cd skills

# 创建新分支
git checkout -b add-new-skill
```

### 2. 创建新技能

```bash
# 复制模板
cp -r template-skill/ your-skill-name/

# 编辑 SKILL.md
cd your-skill-name
```

### 3. 编写 SKILL.md

遵循以下结构：

```markdown
---
name: your-skill-name
description: 清晰描述技能的功能和使用场景（一句话）
---

# Your Skill Name

简短介绍这个技能的用途。

## Instructions

详细的执行步骤：
1. 第一步
2. 第二步
3. 第三步

## Usage Examples

### Example 1: 基础用法
**Input**: 输入示例
**Output**: 输出示例

### Example 2: 高级用法
**Input**: 输入示例
**Output**: 输出示例

## Dependencies

列出依赖：
- 工具/库名称: 版本要求
- 环境要求

## Guidelines

- 最佳实践 1
- 最佳实践 2
- 注意事项
- 错误处理建议
```

### 4. 添加资源文件（可选）

如果需要额外的资源文件：

```bash
mkdir resources
# 添加配置文件、示例代码、模板等
```

### 5. 测试技能

在 Claude Code 中测试：

```bash
# 本地测试
kiro plugins add /path/to/your/skills

# 测试技能
# 在对话中使用你的技能
```

### 6. 提交 Pull Request

```bash
git add .
git commit -m "添加 your-skill-name 技能"
git push origin add-new-skill
```

然后在 GitHub 上创建 Pull Request。

## 技能质量标准

### 必须包含

- [ ] 清晰的 name 和 description
- [ ] 详细的 Instructions
- [ ] 至少 2 个 Usage Examples
- [ ] 明确的 Guidelines

### 建议包含

- [ ] Dependencies 说明
- [ ] 错误处理指导
- [ ] 安全注意事项
- [ ] 性能考虑

### 代码风格

- 使用清晰的标题层级
- 示例要具体可执行
- 避免模糊的描述
- 提供实际的输入输出

## 技能命名规范

- 使用 kebab-case（小写字母，连字符分隔）
- 名称要描述性强
- 避免过于宽泛的名称

好的示例：
- `api-design`
- `test-generator`
- `code-review`

不好的示例：
- `helper`（太宽泛）
- `MySkill`（不是 kebab-case）
- `skill_name`（使用下划线）

## 技能分类

当前技能分类：

- **开发工具**: api-design, test-generator
- **代码质量**: code-review, refactor-assistant
- **文档生成**: （待添加）
- **数据处理**: （待添加）

## 问题反馈

如果发现问题或有建议：

1. 在 GitHub Issues 中创建 issue
2. 描述问题或建议
3. 如果可能，提供复现步骤

## 许可证

贡献的代码将使用 Apache 2.0 许可证。
