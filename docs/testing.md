# 测试规范

本文档定义了使用此脚手架时的测试规范。

## 测试原则

- 所有新功能必须有测试
- 测试应该独立、可重复
- 使用有意义的测试名称

## 后端测试 (Python)

```python
def test_create_user(client):
    """测试创建用户"""
    response = client.post("/users", json={"name": "test"})
    assert response.status_code == 201
    assert response.json()["name"] == "test"
```

运行测试：
```bash
pytest
```

## 前端测试 (TypeScript)

```typescript
describe("UserForm", () => {
  it("should submit valid data", () => {
    // test implementation
  });
});
```

运行测试：
```bash
npm test
```

## 测试覆盖率

- 目标覆盖率：80%+
- 使用 `pytest --cov` 或 `npm test -- --coverage`
