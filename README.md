# Cross-border AI Business Control Tower

> 面向跨境电商运营的数据分析与经营诊断 Demo

## 项目简介

这是一个面向跨境电商运营场景的数据分析系统。它可读取订单、商品、库存与广告报表，按 ASIN、SKU、站点和广告活动等维度整理经营数据，并通过仪表盘、异常清单和自然语言问答帮助运营人员理解业务表现。

用户可以提出诸如“近 30 天哪些 ASIN 销量下滑？”或“哪些广告活动花费高但转化差？”的问题。系统会按相应维度计算指标、定位异常，并生成初步经营建议。

当前 Demo 主要支持 Excel/CSV 数据上传，架构上预留 API 接入能力；不宣称已接入全部真实 Amazon API。

## 项目目标

减少以下重复性人工工作：

- 下载和整理多个经营报表
- 手动合并 Excel
- 逐个检查商品和广告数据
- 人工定位销量、库存及投放异常
- 重复制作经营分析表格

## 核心功能

- 销售趋势分析
- ASIN/SKU 表现分析
- 销量下滑识别
- 库存风险提示
- 广告花费及转化分析
- ACOS 与 ROAS 分析
- 利润表现初步诊断
- 异常结果表格化展示
- 初步运营建议生成

系统用于辅助分析和优先级判断，不自动替代最终商业决策。

## 演示流程

1. 上传订单、商品和广告示例数据。
2. 系统完成字段识别和数据整理。
3. 用户输入自然语言经营问题。
4. 系统按相应维度计算指标。
5. 输出异常清单、分析结果和建议。

## 示例问题

- 近 30 天哪些 ASIN 销量下滑？
- 哪些广告活动花费较高但没有订单？
- 哪些 SKU 的 ACOS 高于可承受水平？
- 哪些商品的 ROAS 表现较弱？
- 哪些 SKU 预计会在补货到达前缺货？
- 哪些商品库存覆盖天数过高？
- 哪些商品退款率高于正常水平？
- 哪些商品贡献利润偏低？
- 销售额与回款金额的差异主要来自哪里？
- 本周最需要处理的三个经营问题是什么？

## 指标说明

| 指标 | 通俗说明 |
| --- | --- |
| Sales | 商品成交金额，通常指报表中的销售额。 |
| Orders | 订单数量。 |
| Units Sold | 已售商品件数。 |
| Conversion Rate | 成交订单相对于访问或点击的比例。 |
| ACOS | 广告花费除以广告归因销售额；越低通常表示投放效率越高。 |
| ROAS | 广告归因销售额除以广告花费；越高通常表示投放回报越好。 |
| Profit Margin | 利润相对于销售额的比例，用于观察盈利空间。 |
| Inventory Coverage | 以当前销售速度估算库存可支持的天数。 |
| Return Rate | 退款或退货件数相对于销售件数的比例。 |

更完整的口径说明见 [docs/metric-definitions.md](docs/metric-definitions.md)。

## 技术架构

- 数据输入层：Excel / CSV
- 数据处理层：Python / SQL / DuckDB
- 分析层：指标计算、规则诊断、自然语言查询
- 展示层：Web Dashboard / Table / Chart
- 部署层：Cloud Web Service

这是高层展示架构，不包含内部接口、实现细节或配置内容。详见 [docs/architecture-overview.md](docs/architecture-overview.md)。

## 在线 Demo

- 在线演示地址：待填写
- 演示视频：待填写

## 数据说明

本仓库中的数据均为模拟或脱敏数据，仅用于产品演示，不包含真实客户、店铺或消费者信息。

## 项目状态

- Demo Version
- Core workflow completed
- API integration reserved for future development

## 仓库说明

本仓库为公开展示版本，不包含生产环境源代码、核心业务逻辑、私有配置、模型密钥或真实业务数据。

## 目录

- [架构概览](docs/architecture-overview.md)
- [演示指南](docs/demo-guide.md)
- [隐私与数据说明](docs/privacy-and-data-note.md)
- [示例数据](demo-data/README.md)
- [示例问题与输出](examples/example-questions.md)
