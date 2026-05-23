# 智择通项目进度管理

## 📊 项目概览

智择通项目采用 GitHub Projects 进行任务管理和进度追踪。

### 项目阶段

| 阶段 | 说明 | 任务示例 |
|------|------|---------|
| 📋 **Backlog** | 待开始的任务 | 新提出的需求、待审批的功能 |
| 🔄 **In Progress** | 正在进行中 | 开发中的功能、正在测试的模块 |
| 👀 **In Review** | 等待审查 | 已提交 PR、等待代码审查 |
| ✅ **Done** | 已完成 | 已合并到主分支、功能已上线 |

---

## 🎯 核心任务列表

### 1️⃣ 数据补充 (`data-collection`)
- **目标**: 补充各省分数线、导师、薪资数据
- **优先级**: P0（高优先级）
- **预计工时**: 2-3周
- **关键交付物**:
  - `data/` 目录结构
  - 数据采集脚本
  - 数据更新日志

### 2️⃣ Agent 开发 (`agent-development`)
- **目标**: 实现7个核心AI Agent
- **优先级**: P0（高优先级）
- **预计工时**: 4-6周
- **7个Agent**:
  1. 数据采集Agent
  2. 导师洞察Agent
  3. 康波周期Agent
  4. 匹配推荐Agent
  5. 评测Agent
  6. 地域价值Agent
  7. 反向溯源Agent

### 3️⃣ UI/UX 优化 (`uiux-design`)
- **目标**: 优化小程序界面
- **优先级**: P1（中优先级）
- **预计工时**: 2-3周
- **关键交付物**:
  - 设计规范文档
  - Figma 原型链接
  - 设计稿提交

### 4️⃣ 国际化支持 (`internationalization`)
- **目标**: 实现多语言与海外院校数据
- **优先级**: P1（中优先级）
- **预计工时**: 2周
- **关键交付物**:
  - i18n 配置文件
  - 中英文语言包
  - 海外数据源集成

### 5️⃣ 案例库建设 (`cases-library`)
- **目标**: 建立择校案例库
- **优先级**: P2（低优先级）
- **预计工时**: 1-2周
- **关键交付物**:
  - `cases/` 目录
  - 至少10个真实案例
  - 案例展示功能

### 6️⃣ 文档与Bug修复 (`docs-bugfix`)
- **目标**: 完善文档、修复已知问题
- **优先级**: P1（中优先级）
- **预计工时**: 1-2周
- **关键交付物**:
  - `docs/` 目录
  - 更新 README
  - Bug 修复清单

---

## 📅 项目时间线

| 阶段 | 时间 | 核心工作 | 状态 |
|------|------|---------|------|
| **Phase 1** | 第1-3周 | 数据补充 + 文档完善 | 🟡 进行中 |
| **Phase 2** | 第4-7周 | Agent开发（前4个Agent） | ⬜ 待开始 |
| **Phase 3** | 第8-10周 | Agent开发（后3个Agent）+ UI优化 | ⬜ 待开始 |
| **Phase 4** | 第11-12周 | 国际化 + 案例库 + 测试 | ⬜ 待开始 |

---

## 🏗️ 项目结构

```
zhizeTong/
├── .github/
│   ├── PROJECT.md                 ← 项目管理文档（本文件）
│   ├── workflows/                 ← GitHub Actions 工作流
│   │   └── ci.yml                 ← CI/CD 配置
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       ├── feature_request.md
│       └── data_contribution.md
├── data/                          ← 数据存储目录
│   ├── README.md                  ← 数据说明
│   ├── scores/                    ← 分数线数据
│   ├── mentors/                   ← 导师数据
│   └── salary/                    ← 薪资数据
├── agents/                        ← Agent 实现
│   ├── __init__.py
│   ├── data_collector.py          ← 数据采集Agent
│   ├── mentor_insight.py          ← 导师洞察Agent
│   ├── kondratiev.py              ← 康波周期Agent
│   ├── matcher.py                 ← 匹配推荐Agent
│   ├── evaluator.py               ← 评测Agent
│   ├── regional_value.py          ← 地域价值Agent
│   └── reverse_trace.py           ← 反向溯源Agent
├── design/                        ← UI/UX 设计
│   ├── README.md
│   ├── figma-links.md
│   └── mockups/
├── cases/                         ← 择校案例库
│   ├── README.md
│   ├── case_001.md
│   ├── case_002.md
│   └── ...
├── docs/                          ← 项目文档
│   ├── README.md
│   ├── API.md
│   ├── ARCHITECTURE.md
│   ├── CONTRIBUTING.md
│   └── DEVELOPMENT.md
├── skill/                         ← 现有技能包
│   ├── SKILL.md
│   └── references/
├── mini-program/                  ← 小程序代码
│   └── ...
├── README.md
├── LICENSE
└── CONTRIBUTING.md
```

---

## 🔗 相关资源

- **GitHub Issues**: [查看所有 Issues](https://github.com/yongqiangbian984-dotcom/zhizeTong/issues)
- **GitHub Projects**: [查看项目看板](https://github.com/yongqiangbian984-dotcom/zhizeTong/projects)
- **虾评技能**: [智择通-大学择校智能决策助手](https://xiaping.coze.com/skill/741e0ff6-d160-453a-8e77-75f671b5e861)

---

## 📌 贡献方式

### 参与任务的流程

1. **选择任务** → 从 Backlog 中选择感兴趣的 Issue
2. **创建分支** → `git checkout -b feature/issue-xxx`
3. **开发实现** → 按照开发规范编写代码
4. **提交 PR** → `git push origin feature/issue-xxx`
5. **代码审查** → 等待维护者审查
6. **合并入库** → 审查通过后合并到 main

### 标签使用规范

- `enhancement` - 新功能、改进
- `bug` - 缺陷修复
- `documentation` - 文档相关
- `data` - 数据相关
- `agent` - Agent 开发
- `design` - UI/UX 设计
- `internationalization` - 国际化
- `help wanted` - 需要帮助
- `good first issue` - 适合新手

---

## 📊 进度统计

| 类别 | 总数 | 完成 | 进行中 | 待开始 |
|------|------|------|--------|--------|
| 核心任务 | 6 | 0 | 0 | 6 |
| 子任务 | 20+ | 0 | 0 | 20+ |
| Bug | 0 | 0 | 0 | 0 |

---

## 📞 沟通方式

- **Issue讨论**: 在对应 Issue 下评论
- **PR审查**: 在 PR 中进行代码审查
- **文档更新**: 提交 PR 更新本文件

---

**最后更新**: 2026-05-23
**维护者**: @yongqiangbian984-dotcom

