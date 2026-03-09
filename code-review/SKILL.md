---
name: code-review
description: 系统化的代码审查技能，检查代码质量、安全性、性能和最佳实践
---

# Code Review Skill

对代码进行全面的审查，提供建设性的反馈和改进建议。

## Instructions

执行代码审查时，按以下顺序检查：

1. **代码质量**
   - 检查命名规范（变量、函数、类）
   - 验证代码结构和组织
   - 识别重复代码
   - 检查函数复杂度

2. **安全性**
   - SQL 注入风险
   - XSS 漏洞
   - 敏感信息泄露
   - 权限验证

3. **性能**
   - 不必要的循环嵌套
   - 数据库查询优化
   - 内存泄漏风险
   - 算法复杂度

4. **最佳实践**
   - 错误处理
   - 日志记录
   - 注释质量
   - 测试覆盖

## Usage Examples

### Example 1: 审查 JavaScript 函数
**Input**: 
```javascript
function getData(id) {
  return fetch('/api/users/' + id).then(r => r.json())
}
```

**Output**:
- 缺少错误处理
- 建议使用模板字符串
- 建议添加类型注释（TypeScript）

### Example 2: 审查 Python 类
**Input**: 包含数据库操作的 Python 类

**Output**:
- SQL 注入风险分析
- 连接池使用建议
- 异常处理改进

## Guidelines

- 提供具体的改进建议，不只是指出问题
- 优先级：安全 > 性能 > 代码质量
- 考虑项目上下文和团队规范
- 给出代码示例说明改进方案
