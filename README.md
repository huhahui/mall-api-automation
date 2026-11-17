# 商城接口自动化测试

基于 Python 的接口自动化测试实践项目，使用 pytest、requests 和 YAML 组织测试，通过本地 Flask 模拟服务练习用户管理和商城业务接口测试。

## 主要功能

- 使用 YAML 维护接口信息、测试数据和预期结果，通过 pytest 参数化执行。
- 封装 HTTP 请求和常见响应断言，支持记录请求和响应信息。
- 使用 JSONPath 提取响应字段，通过占位符将订单编号等数据传递给后续请求。
- 使用 fixture 组织测试前置操作和日志记录，使用 Allure 展示测试结果。
- 提供 Flask 模拟接口，覆盖商品查询、下单、支付及订单状态查询等场景。

## 技术栈

Python、pytest、requests、PyYAML、JSONPath、Allure、Flask。

## 目录结构

```text
base/          # 请求和业务流程封装
common/        # YAML 读取、断言、请求等工具
conf/          # 环境和配置
data/          # 测试数据
testcase/      # 用户管理、商品管理及业务流程用例
mock_server/   # Flask 模拟接口服务
run.py         # 测试运行入口
```

## 运行说明

运行环境、模拟服务和配置需要按 `pyproject.toml` 与 `conf/config.ini` 准备；仓库中的凭据已替换为占位符。运行 `run.py` 会执行测试并尝试使用 Allure 打开报告，测试过程会修改提取数据和报告目录。

模拟支付接口用于测试请求与响应，真实支付状态与资金到账需要独立系统验证。运行前请结合当前环境检查配置及依赖。


