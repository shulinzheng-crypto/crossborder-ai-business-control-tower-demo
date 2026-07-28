CrossBorder AI Business Control Tower

> **一个面向 Amazon 跨境电商的 AI 经营分析与数据治理 Demo**
>
> **Interview Demo by Shulin｜仅供无变科技招聘评估使用**
>
> 演示数据均为合成数据，不包含任何真实客户或买家隐私信息。

---

## 📸 系统预览

> <img width="1049" height="725" alt="image" src="https://github.com/user-attachments/assets/ac6d5834-d7ca-4d90-90d5-a533e4806e4c" />


---

## 🎥 Demo

- 📹请先看演示视频：需在“Datahub”先录入4个excel数据表格进行分析（可接Amazon API） [Demo Video（HR 演示录屏）](https://drive.google.com/file/d/1JRhYbIdOfFZZqPGfYPR4BJTIilnqdlMX/view?usp=drivesdk)
- 💻 GitHub Repository（当前仓库）
- 🌐 [系统demo（在线体验）](https://crossborder-ai-business-control-tower.onrender.com)

---

# 为什么做这个项目？

在跨境电商企业中，运营、广告、仓库和财务通常使用不同的数据口径：

- 商品命名方式不一致；
- 不同系统中的 SKU 无法直接对应；
- 销售额、广告费用、库存和财务结算之间缺乏统一视角；
- 管理者能够看到数据，却很难快速定位经营问题产生的真正原因。

很多时候，一个简单的问题：

> **为什么销量上涨了，但利润反而下降？**

需要运营、广告、财务、供应链分别导出 Excel，再进行人工整理和比对。

因此，我希望构建一个位于 **ERP 与管理层之间** 的 **AI 经营分析层（Business Control Tower）**，帮助团队统一数据口径，快速定位经营问题，并提供可解释的 AI 分析。

---

# 我的解决方案

本项目采用：

> **数据治理 → 数据计算 → AI解释**

而不是：

> **直接把 Excel 丢给 AI。**

整个分析流程如下：

```                Data Sources
────────────────────────────────────
 Orders
 Advertising
 Inventory
 Finance
 Product Master
────────────────────────────────────
                    │
                    ▼
             Data Governance
────────────────────────────────────
 Data Quality
 Master SKU Mapping
 Data Validation
────────────────────────────────────
                    │
                    ▼
          Business Calculation
────────────────────────────────────
 SQL Engine
 Python Metrics
 Revenue
 Profit
 Inventory
────────────────────────────────────
                    │
                    ▼
         AI Decision Layer
────────────────────────────────────
 Evidence-first AI
 Exception Detection
 Weekly Report
────────────────────────────────────
                    │
                    ▼
              User Interface
────────────────────────────────────
 Executive Overview
 Product Center
 Product 360
 Inventory
 Profitability
 AI Assistant
```

其中：

- **SQL / Python** 负责所有经营指标计算；
- **AI** 不负责计算数据，只解释已经验证的数据；
- 每一个 AI 结论都可以追溯到对应的数据来源（Evidence）。

这种设计可以降低 AI 幻觉（Hallucination）带来的业务风险，提高经营分析的可信度。

---

# 核心功能

##  Executive Overview

帮助管理者快速了解整体经营情况，包括：

- 销售额
- 利润
- 广告表现
- 库存状态
- 经营趋势

---

##  Product Center

统一展示所有商品经营信息。

支持查看：

- Master SKU
- ASIN
- 销量
- 利润
- 库存
- 广告表现
- 风险标签

---

##  Product 360

查看单个商品完整经营画像，包括：

- 销售趋势
- 广告数据
- 库存变化
- 财务情况
- AI分析建议

---

##  Data Quality

自动检测数据质量问题：

- 重复订单
- 缺失采购成本
- SKU异常
- 数据完整性问题

---

##  Master SKU Mapping

统一不同系统之间的商品身份，解决：

- SKU名称不同
- 重复商品
- 无法统一统计

等问题。

---

##  Profitability

帮助定位利润变化原因。

包括：

- 销售额
- 商品成本
- 广告费用
- 毛利润
- 利润趋势

---

##  Inventory

分析：

- 库存天数
- 缺货风险
- 建议补货数量

帮助运营提前发现补货风险。

---

##  Exception Center

自动汇总经营异常，包括：

- 高退货率
- 缺失成本
- 库存不足
- 财务差异
- SKU异常

帮助团队快速定位需要优先处理的问题。

---

##  AI Assistant

AI 不负责计算经营数据。

它只负责：

- 总结问题；
- 分析原因；
- 给出优化建议；

所有结论均引用已经计算完成的数据（Evidence-first AI）。

---

# 项目特点

相比传统 BI 或 ERP，本项目更关注：

✅ 数据治理（Data Governance）

✅ Master SKU 统一

✅ 可解释 AI（Explainable AI）

✅ 经营诊断（Business Diagnostics）

✅ 异常定位（Exception Detection）

而不是替代 ERP 本身。

---

# 项目迭代

## V0

完成：

- 基础订单分析
- 库存分析
- 财务分析

目标：

> 能够看到经营数据。

---

## V1

新增：

- Data Quality
- SKU Mapping
- Exception Center
- AI Assistant

目标：

> 能够发现经营问题。

---

## V1.1（当前版本）

继续完善：

- Product Center
- Product 360
- 利润分析
- AI解释
- 双语界面
- 演示流程优化

目标：

> 不仅能够发现问题，还能够解释问题。

---

# 技术架构

| 模块 | 技术 |
|------|------|
| Frontend | Next.js + TypeScript |
| Backend | FastAPI |
| Analytics | SQL + Python |
| Database | DuckDB |
| Charts | Recharts |
| Tables | TanStack Table |
| AI | OpenAI-compatible API |

---

# Demo 数据

仓库提供完整的合成演示数据。

包括：

- Orders
- Inventory
- Finance

为了完整展示经营分析流程，数据中故意设计了：

- 重复订单
- 缺失采购成本
- 高退货率
- 库存风险
- SKU映射问题
- 财务差异

所有数据均为合成数据，不包含真实买家信息。

---

# 项目结构

```text
apps/
├── api/                FastAPI 后端
├── web/                Next.js 前端

data/
├── demo/               合成演示数据

docs/
├── contracts/          API 与数据契约
├── architecture/       系统设计文档
├── reports/            项目报告

scripts/                初始化与维护脚本
```

---

# 快速开始

## 安装依赖

```bash
cp .env.example .env

make setup
```

---

## 启动项目

```bash
make dev
```

启动后访问：

- Web：http://127.0.0.1:3000
- API：http://127.0.0.1:8000/docs

---

# 常用命令

```bash
make dev            # 启动前后端
make test           # 运行测试
make build          # 生产构建
make db-init        # 初始化 DuckDB
make data-generate  # 重建演示数据
```

---

# 安全说明

本项目遵循以下原则：

- 不保存买家姓名、电话、地址等 PII；
- `.env` 不进入 Git；
- AI 不参与经营指标计算；
- 所有经营指标均由 SQL / Python 计算；
- 未配置真实接口时返回可验证的 Demo 数据。

---


# 项目规划（Roadmap）

虽然当前版本主要用于展示跨境电商经营分析的核心能力，但我希望它未来能够逐步演进为一个真正服务于 Amazon 精品运营团队的 AI Business Control Tower。

## Phase 1（当前版本）✅

已完成核心经营分析能力，包括：

- Executive Overview（经营总览）
- Product Center（商品中心）
- Product 360（商品全景分析）
- Data Quality（数据质量检查）
- Master SKU Mapping（统一商品身份）
- Profitability（利润分析）
- Inventory（库存分析）
- Exception Center（经营异常中心）
- AI Assistant（AI经营分析助手）
- Weekly Report（经营周报）
- 中英文双语界面
- Synthetic Demo Dataset（合成演示数据）

---

## Phase 2（数据接入）

计划接入真实业务数据，实现自动化分析：

- Amazon SP-API Integration
- Amazon Ads API Integration
- 自动数据同步
- 多店铺管理（Multi-store Management）
- 自定义 Dashboard
- Analysis Run（分析版本管理）

---

## Phase 3（经营分析增强）

进一步扩展经营分析能力：

- Revenue-to-Cash（订单到回款分析）
- Returns & Refunds（退货与退款分析）
- Expense Management（费用管理）
- Cash Flow（现金流分析）
- Supplier Performance（供应商表现）
- Procurement & Replenishment（采购与补货建议）
- Pricing Analysis（价格分析）
- Search Terms Analysis（搜索词分析）
- Advertising Attribution（广告归因分析）

---

## Phase 4（AI Copilot）

进一步增强 AI 在经营分析中的作用：

- AI 自动生成经营周报
- AI 自动发现经营异常
- AI 根因分析（Root Cause Analysis）
- AI 优化建议
- 自定义 KPI 问答
- 多轮业务分析对话
- AI Action Plan（自动生成执行方案）

---

## Phase 5（企业协作）

支持团队协作与企业级管理：

- 多角色权限（RBAC）
- 审批流程
- 评论与协作
- 异常工单（Issue Tracking）
- Slack / 企业微信通知
- 邮件自动发送周报
- 审计日志（Audit Log）

---

## 长期愿景（Vision）

CrossBorder AI Business Control Tower 并不是一个 ERP，也不是一个传统 BI。

我的目标是构建一个位于 **Amazon 平台、企业内部数据与管理层之间** 的 **AI 经营分析与数据治理层（AI Business Intelligence & Data Governance Layer）**。

它负责统一来自订单、广告、库存、财务等不同来源的数据，通过标准化的数据治理、可解释的经营指标计算以及 Evidence-first AI 分析，为运营、广告、供应链和财务团队提供统一的经营视角，帮助团队更快地发现问题、定位原因并辅助决策，而不仅仅是展示数据。

---

# 关于本项目

本项目由 **Shulin** 独立设计与开发，用于展示：

- 产品设计能力
- 数据治理能力
- AI 应用能力
- 全栈开发能力
- 跨境电商业务分析能力

---

> **Interview Demo**
>
> **仅供无变科技招聘评估使用。**
>
> **演示数据均为合成数据。**
