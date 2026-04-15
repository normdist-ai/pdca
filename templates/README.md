# PDCA 模板库

> 本目录包含PDCA技能的所有模板文件，按照用途和场景分类组织。

---

## 📁 目录结构

```
templates/
├── README.md                          # 本说明文件
├── issue-template.md                  # 问题概述模板
├── generic/                           # 通用阶段模板
│   ├── plan-template.md               # Plan阶段通用模板
│   ├── do-template.md                 # Do阶段通用模板
│   ├── check-template.md              # Check阶段通用模板
│   └── act-template.md                # Act阶段通用模板
└── scenarios/                         # 场景专用模板
    ├── bugfix/                        # BUG修复场景
    │   ├── template.md                # BUG修复PDCA模板
    │   ├── example.md                 # 使用示例
    │   └── README.md                  # 场景说明（回归测试强化）
    ├── feature-dev/                   # 功能开发场景
    │   └── template.md                # 功能开发PDCA模板
    ├── software-plan/                 # 制定软件开发计划场景
    │   └── template.md                # 制定计划PDCA模板
    ├── code-review/                   # 代码审查场景
    │   └── template.md                # 代码审查PDCA模板
    └── performance-opt/               # 性能优化场景
        └── template.md                # 性能优化PDCA模板
```

---

## 📋 模板分类

### 1. 通用阶段模板（generic/）

这些模板提供PDCA四个阶段的基础结构和指导，适用于任何PDCA循环。

- **[plan-template.md](generic/plan-template.md)** - Plan阶段通用模板
  - SMART目标设定
  - WBS工作分解
  - SIPOC过程分析
  - SWOT风险评估

- **[do-template.md](generic/do-template.md)** - Do阶段通用模板
  - 任务执行记录
  - 进度跟踪
  - 文档管理
  - 问题清单

- **[check-template.md](generic/check-template.md)** - Check阶段通用模板
  - 结果验证
  - 偏差分析
  - 5WHY根因分析
  - 数据统计

- **[act-template.md](generic/act-template.md)** - Act阶段通用模板
  - 经验总结
  - 标准化
  - 持续改进
  - 知识库更新

**使用建议**：当没有合适的场景模板时，使用通用模板。

---

### 2. 场景专用模板（scenarios/）

这些模板针对特定的软件开发场景进行了优化，提供更具体的指导和检查清单。

#### 🐛 BUG修复（scenarios/bugfix/）

**[template.md](scenarios/bugfix/template.md)** - BUG修复PDCA模板

**特点**：
- 强调根因分析（5WHY方法）
- 详细的回归测试检查清单
- 注重知识沉淀和预防措施
- 支持代码修改和问题文档的双重输出

**相关文件**：
- [example.md](scenarios/bugfix/example.md) - 实际案例演示
- [README.md](scenarios/bugfix/README.md) - 回归测试强化说明

**适用场景**：
- 功能性BUG修复
- 性能问题优化
- 安全漏洞修补
- 用户体验问题改进

---

#### 💻 功能开发（scenarios/feature-dev/）

**[template.md](scenarios/feature-dev/template.md)** - 功能开发PDCA模板

**特点**：
- 从用户故事出发，明确验收标准
- 完整的技术方案设计（架构、数据模型、API）
- 强调测试覆盖率（单元、集成、回归）
- 代码质量检查（静态分析、代码审查）
- 性能和安全审查

**适用场景**：
- 新功能开发
- 用户故事实现
- 功能增强
- API接口开发

---

#### 📋 制定软件开发计划（scenarios/software-plan/）

**[template.md](scenarios/software-plan/template.md)** - 制定软件开发计划PDCA模板

**特点**：
- **纯文档输出**，不涉及代码开发
- 属于顶层PDCA的Plan阶段，本身也是一个PDCA循环
- 完整的需求分析和优先级排序
- 详细的工作量估算和资源计划
- 全面的风险评估和应对策略
- 干系人评审和基线化管理

**适用场景**：
- 新项目启动
- 迭代/Sprint计划制定
- 版本发布计划
- 重大项目变更规划

**注意**：此模板的输出物是计划文档，不是代码！

---

#### 🔍 代码审查（scenarios/code-review/）

**[template.md](scenarios/code-review/template.md)** - 代码审查PDCA模板

**特点**：
- 多维度审查（功能性、可读性、可维护性、性能、安全）
- 静态分析工具集成
- 自动化测试验证
- 问题分类和严重程度评级
- 优秀实践记录和推广

**适用场景**：
- 代码合并前审查（Pull Request/Merge Request）
- 定期代码质量检查
- 重构后的代码验证
- 新人代码指导和培训
- 技术债务识别和评估

---

#### ⚡ 性能优化（scenarios/performance-opt/）

**[template.md](scenarios/performance-opt/template.md)** - 性能优化PDCA模板

**特点**：
- 性能基线建立和监控
- 根因分析（Profiling + 5WHY）
- 多种优化策略对比
- 成本效益分析（ROI）
- 副作用检查和回归测试
- 可持续性评估

**适用场景**：
- 系统响应慢优化
- 吞吐量提升
- 资源利用率优化
- 数据库性能调优
- 前端性能优化

---

### 3. 问题概述模板

**[issue-template.md](issue-template.md)** - 问题概述模板

用于创建新的PDCA问题时，记录问题的基本信息和PDCA循环的索引。

---

## 🎯 如何选择模板

### 决策流程

```
开始
  ↓
是否有特定场景？
  ├─ 是 → 选择对应的场景模板
  │        ├─ BUG修复 → scenarios/bugfix/template.md
  │        ├─ 功能开发 → scenarios/feature-dev/template.md
  │        ├─ 制定计划 → scenarios/software-plan/template.md
  │        ├─ 代码审查 → scenarios/code-review/template.md
  │        └─ 性能优化 → scenarios/performance-opt/template.md
  │
  └─ 否 → 使用通用模板
           ├─ Plan阶段 → generic/plan-template.md
           ├─ Do阶段 → generic/do-template.md
           ├─ Check阶段 → generic/check-template.md
           └─ Act阶段 → generic/act-template.md
```

### 使用建议

1. **优先使用场景模板**：场景模板提供了更具体的指导和检查清单
2. **参考示例文件**：部分场景模板提供了实际案例（如BUG修复）
3. **阅读场景说明**：某些场景有特殊注意事项（如回归测试强化）
4. **灵活组合使用**：可以根据需要组合不同模板的元素

---

## 📖 使用指南

### 基本使用流程

1. **复制模板**：从相应目录复制模板文件
2. **填充内容**：根据具体情况填写模板中的占位符
3. **执行PDCA**：按照模板指导完成四个阶段
4. **保存记录**：保存到 `.pdca/issues/issue-xxxxx/` 目录
5. **更新索引**：在 `issue-list.md` 中添加记录

### 示例：BUG修复

```bash
# 1. 复制模板
cp templates/scenarios/bugfix/template.md .pdca/issues/issue-20260415-xxx/bugfix-plan.md

# 2. 编辑模板，填充具体内容
# ... 编辑文件 ...

# 3. 按照PDCA四个阶段执行
# Plan: 分析问题，制定修复方案
# Do: 实施代码修复
# Check: 验证修复效果，执行回归测试
# Act: 总结经验，更新知识库

# 4. 保存并更新索引
```

---

## 🔄 模板维护

### 添加新场景模板

1. 在 `scenarios/` 下创建新文件夹：`scenarios/new-scenario/`
2. 创建主模板：`scenarios/new-scenario/template.md`
3. （可选）创建示例：`scenarios/new-scenario/example.md`
4. （可选）创建说明：`scenarios/new-scenario/README.md`
5. 更新本README文件，添加新场景说明
6. 更新 `SKILL.md` 中的模板列表

### 更新现有模板

1. 直接编辑对应的模板文件
2. 如果有重大变更，更新本README中的说明
3. 同步更新 `SKILL.md` 中的相关描述

---

## 🔗 相关链接

- [PDCA技能说明](../SKILL.md)
- [.pdca 目录说明](../.pdca/README.md)
- [AgentSkills规范](https://agentskills.io/specification)

---

*最后更新: 2026-04-15*
