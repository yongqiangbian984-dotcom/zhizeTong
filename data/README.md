# 数据目录 📊

本目录存放智择通平台所需的各类数据资源，包括分数线、导师信息、行业薪资等。

## 📁 目录结构

```
data/
├── README.md                      ← 本文件
├── scores/                        ← 分数线数据
│   ├── provincial/                ← 各省份分数线
│   ├── universities/              ← 高校录取线
│   └── majors/                    ← 专业录取线
├── mentors/                       ← 导师数据
│   ├── profiles/                  ← 导师个人信息
│   ├── papers/                    ← 论文发表记录
│   └── student_reviews/           ← 学生评价
└── salary/                        ← 行业薪资数据
    ├── by_industry/               ← 按行业分类
    ├── by_region/                 ← 按地区分类
    └── by_position/               ← 按岗位分类
```

## 📝 数据来源

| 数据类型 | 推荐来源 | 更新频率 |
|---------|--------|--------|
| 分数线 | 教育部官网、高校官网 | 年度（6月-8月） |
| 导师信息 | 高校官网、科研平台 | 持续更新 |
| 薪资数据 | 智联招聘、BOSS直聘、牛客网 | 月度更新 |

## 📦 数据格式

### 分数线数据 (CSV/JSON)

```json
{
  "year": 2024,
  "province": "北京",
  "university": "清华大学",
  "major": "计算机科学与技术",
  "score": 680,
  "rank": 150
}
```

### 导师数据 (JSON)

```json
{
  "id": "mentor_001",
  "name": "张三",
  "university": "清华大学",
  "department": "计算机系",
  "research_area": "人工智能",
  "papers": [
    "Paper Title 1",
    "Paper Title 2"
  ],
  "student_count": 8,
  "student_reviews": 4.5
}
```

### 薪资数据 (CSV)

```csv
position,company,city,salary_min,salary_max,year
软件工程师,BAT,北京,30,60,2024
产品经理,字节跳动,杭州,35,70,2024
```

## 🔄 数据更新流程

1. **数据收集** → 从各来源采集最新数据
2. **数据清洗** → 验证数据准确性、去重、格式化
3. **数据验证** → 人工审核关键数据
4. **提交 PR** → 创建 Pull Request，描述数据变更
5. **合并入库** → 审查通过后合并到 main 分支

## 📋 贡献指南

欢迎贡献数据！请：

1. Fork 本仓库
2. 创建数据分支：`git checkout -b data/add-xxx`
3. 添加或更新数据文件
4. 提交 commit：`git commit -m "data: 补充xxx数据"`
5. 推送并创建 PR

## ⚠️ 数据使用注意事项

- ✅ 所有数据必须来自公开渠道或经过授权
- ✅ 涉及个人信息的数据需匿名处理
- ✅ 必须注明数据来源和更新时间
- ✅ 遵守各数据源的使用协议

## 📞 问题反馈

如发现数据错误或过期，请：
- 提交 Issue：描述具体问题和建议的数据来源
- 直接 PR：纠正错误数据

---

**维护者**: @yongqiangbian984-dotcom  
**最后更新**: 2026-05-23
