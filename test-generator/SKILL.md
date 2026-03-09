---
name: test-generator
description: 为代码生成单元测试、集成测试和端到端测试，支持多种测试框架
---

# Test Generator Skill

自动生成高质量的测试代码，提高测试覆盖率。

## Instructions

生成测试时：

1. **分析代码结构**
   - 识别函数/方法
   - 确定输入输出
   - 找出边界条件
   - 识别依赖项

2. **测试用例设计**
   - 正常情况测试
   - 边界值测试
   - 异常情况测试
   - Mock 外部依赖

3. **测试框架选择**
   - JavaScript: Jest, Mocha, Vitest
   - Python: pytest, unittest
   - Java: JUnit, TestNG
   - Go: testing package

4. **断言设计**
   - 验证返回值
   - 验证副作用
   - 验证异常抛出

## Usage Examples

### Example 1: JavaScript 函数测试
**Input**:
```javascript
function add(a, b) {
  return a + b;
}
```

**Output**:
```javascript
describe('add', () => {
  it('should add two positive numbers', () => {
    expect(add(2, 3)).toBe(5);
  });
  
  it('should handle negative numbers', () => {
    expect(add(-1, 1)).toBe(0);
  });
  
  it('should handle zero', () => {
    expect(add(0, 5)).toBe(5);
  });
});
```

### Example 2: API 端点测试
**Input**: Express.js 路由处理器

**Output**: 包含 Mock 请求/响应的集成测试

## Guidelines

- 每个函数至少 3 个测试用例
- 测试名称清晰描述测试内容
- 使用 AAA 模式（Arrange, Act, Assert）
- Mock 外部依赖（数据库、API）
- 测试应该独立、可重复
