# 贡献指南

感谢你对智择通的关注！以下是如何参与贡献的指南。

## 🎯 我们最需要的贡献

### 高优先级
1. **数据补充**
   - 各省份历年高考分数线数据（JSON/CSV格式）
   - 国内/海外院校基础数据
   - 行业薪资地域差数据
   - 导师公开数据（论文/项目/学生去向）

2. **Agent 实现**
   - 数据采集Agent（Data Agent）：自动抓取排名/分数线/导师数据
   - 导师洞察Agent（Mentor Agent）：分析导师学术影响力+人脉+行业连接
   - 康波周期Agent（Konjun Agent）：经济周期追踪+行业趋势预判
   - 匹配推荐Agent（Match Agent）：多维匹配算法
   - 地域价值Agent（Region Agent）：地域时间价值计算

3. **Bug修复**
   - 产品框架文档中的数据错误
   - 评分模型逻辑问题
   - 参考数据过时

### 中优先级
4. **案例补充**：更多真实的择校决策案例
5. **国际化**：海外院校数据、英文文档
6. **UI/UX**：小程序界面设计优化

## 📋 贡献流程

1. Fork 本仓库
2. 创建分支：`git checkout -b feature/your-feature`
3. 提交改动：`git commit -m "Add: your feature description"`
4. 推送分支：`git push origin feature/your-feature`
5. 创建 Pull Request

## 📝 提交规范

- `Add:` 新增功能/数据/文档
- `Fix:` 修复错误
- `Update:` 更新已有内容
- `Refactor:` 重构/优化

## 💬 讨论与建议

- 使用 GitHub Issues 提交问题和建议
- 标签说明：`data`（数据相关）、`agent`（Agent开发）、`docs`（文档）、`bug`（错误）

## 📊 数据贡献格式

### 院校数据
```json
{
  "name": "学校名称",
  "type": "985/211/双一流/一本/二本/专科",
  "province": "省份",
  "city": "城市",
  "ranking": {
    "qs": 0,
    "times": 0,
    "us_news": 0
  },
  "scores": {
    "2024": { "province": { "文科": 0, "理科": 0 } }
  }
}
```

### 导师数据
```json
{
  "name": "导师姓名",
  "university": "所属学校",
  "department": "院系",
  "title": "职称",
  "research_areas": ["研究方向"],
  "h_index": 0,
  "projects": ["国家级项目"]
}
```

感谢你的贡献！每一个PR都会被认真对待。
