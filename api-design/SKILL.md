---
name: api-design
description: 设计 RESTful API，包括路由规划、请求/响应格式、错误处理和文档生成
---

# API Design Skill

帮助设计清晰、一致、易用的 RESTful API。

## Instructions

设计 API 时遵循以下步骤：

1. **资源识别**
   - 确定核心资源（名词）
   - 定义资源关系
   - 规划 URL 结构

2. **HTTP 方法映射**
   - GET: 获取资源
   - POST: 创建资源
   - PUT/PATCH: 更新资源
   - DELETE: 删除资源

3. **请求/响应设计**
   - 统一的数据格式（JSON）
   - 分页、过滤、排序
   - 字段选择

4. **错误处理**
   - 标准 HTTP 状态码
   - 错误响应格式
   - 错误消息国际化

5. **版本控制**
   - URL 版本 vs Header 版本
   - 向后兼容策略

## Usage Examples

### Example 1: 用户管理 API
**Input**: 需要设计用户 CRUD API

**Output**:
```
GET    /api/v1/users          # 获取用户列表
GET    /api/v1/users/:id      # 获取单个用户
POST   /api/v1/users          # 创建用户
PUT    /api/v1/users/:id      # 更新用户
DELETE /api/v1/users/:id      # 删除用户
```

### Example 2: 嵌套资源
**Input**: 用户的订单管理

**Output**:
```
GET /api/v1/users/:userId/orders
POST /api/v1/users/:userId/orders
```

## Dependencies

- OpenAPI/Swagger 规范知识
- HTTP 协议理解
- JSON Schema

## Guidelines

- 使用复数名词表示资源集合
- URL 中只使用名词，不使用动词
- 保持 URL 层级简单（不超过 3 层）
- 提供完整的 API 文档
- 考虑 API 的可测试性
