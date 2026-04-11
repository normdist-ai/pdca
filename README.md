# PDCA 技能

基于ISO9000标准的PDCA循环方法论技能，指导代理按照策划、实施、检查、处置四个阶段系统化开展工作，帮助用户实现持续改进。

## 📖 简介

PDCA循环（Plan-Do-Check-Act）是ISO9000质量管理体系标准中的核心方法论，由美国质量管理专家戴明博士推广，因此也称为"戴明环"。本技能将PDCA理论应用于软件开发和项目管理，帮助用户系统化地解决问题、持续改进流程。

## 🎯 核心功能

### 四阶段方法论

| 阶段 | 英文 | 核心目标 | 关键活动 |
|------|------|----------|----------|
| 📋 **Plan** | 策划 | 建立目标和过程 | SMART目标设定、WBS分解、SIPOC分析 |
| ⚙️ **Do** | 实施 | 执行策划方案 | 任务执行、进度跟踪、文档管理 |
| 🔍 **Check** | 检查 | 监视和测量结果 | 结果验证、偏差分析、5WHY根因分析 |
| 🔄 **Act** | 处置 | 持续改进绩效 | 经验总结、标准化、制定改进措施 |

### 配套工具

- **SMART**：目标设定（具体的、可衡量的、可实现的、相关的、有时限的）
- **WBS**：工作分解结构（里程碑、工作包）
- **SIPOC**：过程分析（供方、输入、过程、输出、顾客）
- **5WHY**：根因分析（连续追问"为什么"）
- **SWOT**：风险识别（优势、劣势、机会、威胁）
- **MECE**：分类穷尽（相互独立、完全穷尽）

## 🚀 快速开始

### 安装

将本技能放置在 `.trae/skills/pdca/` 目录下即可自动加载。

### 使用方法

在对话中提到以下关键词即可激活PDCA技能：

- `PDCA`、`PDCA循环`、`戴明环`
- `持续改进`、`质量管理`
- `项目策划`、`问题解决`、`流程改进`

### 示例

```
用户：我想用PDCA方法改进代码审查流程
代理：[按照PDCA四阶段帮助用户开展工作]

用户：/pdca 优化项目管理流程
代理：[启动PDCA循环，创建问题文件夹，记录过程]
```

## 📁 目录结构

### 输出目录（.pdca/）

```
项目根目录/
└── .pdca/
    ├── issue-list.md          # 问题索引列表
    └── issues/                # 问题文件夹
        ├── issue-20260409-143000/  # 问题1
        │   ├── README.md      # 问题概述
        │   ├── plan/          # Plan阶段文件
        │   ├── do/            # Do阶段文件
        │   ├── check/         # Check阶段文件
        │   └── act/           # Act阶段文件
        └── issue-20260410-150000/  # 问题2
            └── ...
```

### 技能目录（.trae/skills/pdca/）

```
.trae/skills/pdca/
├── SKILL.md                   # 技能主文件
├── templates/                 # 模板文件夹
│   ├── issue-template.md      # 问题概述模板
│   ├── plan-template.md       # Plan阶段模板
│   ├── do-template.md         # Do阶段模板
│   ├── check-template.md      # Check阶段模板
│   └── act-template.md        # Act阶段模板
├── references/                # 参考文档
│   ├── theory.md              # 理论基础
│   ├── example.md             # 完整示例
│   ├── templates.md           # 实用模板
│   ├── checklists.md          # 检查清单
│   ├── metrics.md             # 度量指标
│   ├── faq.md                 # 常见问题
│   └── glossary.md            # 术语表
└── assets/                    # 资产文件
    ├── agentskills-checklist.md
    └── skill-description-guidelines.md
```

## 📚 文档

- **[理论基础](.trae/skills/pdca/references/theory.md)**：PDCA理论详解、四个阶段详细说明、配套工具方法
- **[完整示例](.trae/skills/pdca/references/example.md)**：代码审查流程改进的完整PDCA循环案例
- **[实用模板](.trae/skills/pdca/references/templates.md)**：SMART目标模板、WBS模板、SIPOC模板、5WHY模板
- **[检查清单](.trae/skills/pdca/references/checklists.md)**：Plan、Do、Check、Act各阶段检查清单
- **[度量指标](.trae/skills/pdca/references/metrics.md)**：效果度量指标、过程度量指标、使用指南
- **[常见问题](.trae/skills/pdca/references/faq.md)**：12个常见问题解答
- **[术语表](.trae/skills/pdca/references/glossary.md)**：PDCA术语中英文对照，107个专业术语

## 🔧 应用场景

### 场景一：项目管理

**Plan**：制定项目章程、WBS、进度计划  
**Do**：执行项目任务、监控进度  
**Check**：阶段评审、验收测试  
**Act**：项目总结、经验归档

### 场景二：问题解决

**Plan**：定义问题、分析原因、制定对策  
**Do**：实施改进措施  
**Check**：验证效果、确认根因消除  
**Act**：标准化、预防再发

### 场景三：流程改进

**Plan**：识别改进机会、设定改进目标  
**Do**：实施新流程、培训人员  
**Check**：评估流程绩效、收集反馈  
**Act**：固化流程、持续优化

## ⚠️ 注意事项

1. **闭环思维**：必须完成完整的PDCA循环，不能只做前两个阶段
2. **数据驱动**：检查阶段必须基于客观数据，不能主观臆断
3. **持续改进**：处置阶段要为下一循环设定更高目标
4. **全员参与**：鼓励团队成员参与PDCA各阶段
5. **文档记录**：每个阶段都要形成规范的文档记录

## 📊 版本历史

| 版本 | 日期 | 主要更新 |
|------|------|----------|
| 2.4 | 2026-04-11 | 优化问题编号规则：is -> issue |
| 2.3 | 2026-04-11 | 重构输出目录结构，创建issues文件夹 |
| 2.2 | 2026-04-10 | 基于SIPOC分析优化模板文件位置 |
| 2.1 | 2026-04-09 | 添加模板、检查清单、度量指标、FAQ |
| 2.0 | 2026-04-09 | 符合AgentSkills规范，添加中英文术语表 |
| 1.0 | 2026-04-09 | 初始版本 |

## 📖 参考资料

- ISO 9000:2015 质量管理体系 基础和术语
- ISO 9001:2015 质量管理体系 要求
- 戴明《走出危机》
- 《质量管理学》
- [AgentSkills规范](https://agentskills.io/specification)

## 📄 许可证

MIT License

## 👤 作者

小翠 - 软件开发团队负责人

## 🔗 相关链接

- [GitHub仓库](https://github.com/normdist-ai/pdca)
- [AgentSkills规范](https://agentskills.io/specification)

---

**让PDCA成为您的持续改进利器！** 🚀
