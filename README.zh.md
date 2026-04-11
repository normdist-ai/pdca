# PDCA 技能

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skill Type](https://img.shields.io/badge/Type-SKILL-blue.svg)](https://agentskills.io)
[![Version](https://img.shields.io/badge/Version-1.7.4-green.svg)](https://github.com/normdist-ai/pdca)

[English Documentation](README.md)

基于ISO9000标准的PDCA循环方法论技能，指导代理按照策划、实施、检查、处置四个阶段系统化开展工作，帮助用户实现持续改进。

## 概述

本技能遵循 Agent Skills 开放标准，完全支持 OpenClaw 平台，并兼容 Trae、Cursor、VS Code、Claude Code 等主流 IDE。当触发时，代理读取技能指令，按照 PDCA 四阶段系统化开展工作，帮助用户实现持续改进。

## 兼容性

### 支持的 IDE

本技能完全兼容以下 IDE：

| IDE | 支持状态 | Skills 目录 |
|------|----------|-------------|
| Trae | ✅ 完全支持 | `.trae/skills/` |
| Cursor | ✅ 完全支持 | `.cursor/skills/` |
| VS Code | ✅ 完全支持 | `.vscode/skills/` |
| OpenCode | ✅ 完全支持 | `~/.config/opencode/skills/` |
| Lingma | ✅ 完全支持 | `.lingma/skills/` |
| Windsurf | ✅ 完全支持 | `.windsurf/skills/` |
| Claude Code | ✅ 完全支持 | `~/.config/claude-code/skills/` |

### 支持的 Agent 平台

本技能可在以下 Agent 平台上运行：

| 平台 | 支持状态 | 说明 |
|------|----------|------|
| OpenClaw | ✅ 完全支持 | 推荐平台 - 开源自托管 Agent 平台，完美支持渐进式披露 |
| Claude Code | ✅ 完全支持 | Anthropic 官方 CLI 工具 |
| 其他 Agent 框架 | ✅ 兼容 | 任何支持 SKILL.md 规范的框架 |

## 技术特性

- ✅ **SKILL.md v3.0 规范**：完全符合最新标准
- ✅ **渐进式披露**：Metadata → Instructions → References，减少 token 消耗
- ✅ **跨平台支持**：Windows (PowerShell) + Linux/macOS (Bash)
- ✅ **标准化输出**：统一的问题文件夹结构，便于追溯和管理
- ✅ **完整文档**：理论基础、完整示例、检查清单、度量指标、FAQ、术语表

## 支持的方法论工具

| 工具 | 用途 | 应用阶段 |
|------|------|----------|
| **SMART** | 目标设定（具体的、可衡量的、可实现的、相关的、有时限的） | Plan |
| **WBS** | 工作分解结构（里程碑、工作包） | Plan |
| **SIPOC** | 过程分析（供方、输入、过程、输出、顾客） | Plan/Do |
| **5WHY** | 根因分析（连续追问"为什么"） | Check |
| **SWOT** | 风险识别（优势、劣势、机会、威胁） | Plan |
| **MECE** | 分类穷尽（相互独立、完全穷尽） | Plan/Check |

## 安装

### 安装指令

当用户请求安装此技能时（如：`安装 https://github.com/normdist-ai/pdca`），请按以下步骤执行：

1. **克隆仓库**（必须使用 git clone，不要下载 ZIP）：
   ```bash
   git clone https://github.com/normdist-ai/pdca.git
   ```

2. **检测当前 IDE**：根据项目目录中存在的配置文件夹判断（如 `.trae/`、`.cursor/`、`.vscode/` 等）

3. **复制到对应 skills 目录**：将克隆的 `pdca` 文件夹复制到 IDE 的 skills 目录下，确保最终路径为 `{skills_dir}/pdca/`

### 各 IDE Skills 目录

| IDE | Skills 目录 | 检测标志 |
|------|-------------|----------|
| Trae | `.trae/skills/pdca` | 存在 `.trae/` 文件夹 |
| Cursor | `.cursor/skills/pdca` | 存在 `.cursor/` 文件夹 |
| VS Code | `.vscode/skills/pdca` | 存在 `.vscode/` 文件夹 |
| OpenCode | `~/.config/opencode/skills/pdca` | Linux/macOS 默认路径 |
| Lingma | `.lingma/skills/pdca` | 存在 `.lingma/` 文件夹 |
| Windsurf | `.windsurf/skills/pdca` | 存在 `.windsurf/` 文件夹 |
| Claude Code | `~/.config/claude-code/skills/pdca` | Claude Code CLI 环境 |

### 安装示例

```bash
# 克隆仓库
git clone https://github.com/normdist-ai/pdca.git

# 复制到 Trae IDE（示例）
cp -r pdca .trae/skills/

# 或复制到 Cursor IDE
cp -r pdca .cursor/skills/

# Windows PowerShell 示例
Copy-Item -Recurse pdca .trae\skills\
```

### 安装验证

安装完成后，skills 目录结构应为：
```
{skills_dir}/pdca/
├── SKILL.md           # 技能定义文件（必需）
├── assets/            # 资产文件
├── references/        # 参考文档
└── templates/         # 模板文件
```

## 使用方法

### 触发短语

当您提到以下关键词时，技能将自动触发：

- `PDCA`、`PDCA循环`、`戴明环`
- `持续改进`、`质量管理`
- `项目策划`、`问题解决`、`流程改进`

### 示例交互

```
用户：我想用PDCA方法改进代码审查流程

代理：我来帮您启动PDCA循环，改进代码审查流程。
     
     📋 Plan 策划阶段
     让我们先明确目标...
     
     [执行策划阶段活动]
     
     ✓ 目标已确定，进入实施阶段...
```

```
用户：/pdca 优化项目管理流程

代理：[启动PDCA循环，创建问题文件夹，记录过程]
```

## 项目结构

```
pdca/
├── SKILL.md                   # 技能定义（代理指令）
├── README.md                  # 项目说明
├── LICENSE                    # MIT 许可证
├── assets/                    # 资产文件
│   ├── agentskills-checklist.md
│   ├── skill-description-guidelines.md
│   └── skill-usage-checklist.md
├── references/                # 参考文档
│   ├── checklists.md          # 检查清单
│   ├── example.md             # 完整示例
│   ├── faq.md                 # 常见问题
│   ├── glossary.md            # 术语表
│   ├── metrics.md             # 度量指标
│   ├── templates.md           # 实用模板
│   └── theory.md              # 理论基础
└── templates/                 # 模板文件夹
    ├── act-template.md        # Act 阶段模板
    ├── check-template.md      # Check 阶段模板
    ├── do-template.md         # Do 阶段模板
    ├── issue-template.md      # 问题概述模板
    └── plan-template.md       # Plan 阶段模板
```

## 工作原理

1. **触发**：代理检测到需要 PDCA 方法论支持
2. **加载**：代理读取 SKILL.md 获取详细指令
3. **执行**：按照 Plan → Do → Check → Act 四阶段开展工作
4. **输出**：在项目根目录创建 `.pdca/` 文件夹，记录完整过程

## 四阶段方法论

| 阶段 | 中文名称 | 核心目标 | 关键活动 | 主要输出 |
|------|------|----------|----------|----------|
| **Plan** | 策划 | 建立目标和过程 | SMART目标设定、WBS分解、SIPOC分析 | 目标说明书、WBS、流程图 |
| **Do** | 实施 | 执行策划方案 | 任务执行、进度跟踪、文档管理 | 执行记录、进度报告、问题清单 |
| **Check** | 检查 | 监视和测量结果 | 结果验证、偏差分析、5WHY根因分析 | 检查报告、偏差分析表、根因记录 |
| **Act** | 处置 | 持续改进绩效 | 经验总结、标准化、制定改进措施 | 经验总结、标准化文件、改进计划 |

## 应用场景

| 场景 | Plan | Do | Check | Act |
|------|------|-----|-------|-----|
| **项目管理** | 制定章程 | 执行监控 | 阶段评审 | 总结归档 |
| **问题解决** | 定义对策 | 实施改进 | 验证根因 | 标准化预防 |
| **流程改进** | 识别机会 | 实施新流程 | 评估绩效 | 固化优化 |

## 注意事项

1. **闭环思维**：必须完成完整的PDCA循环，不能只做前两个阶段
2. **数据驱动**：检查阶段必须基于客观数据
3. **持续改进**：处置阶段要为下一循环设定更高目标

## 版本历史

| 版本 | 日期 | 主要更新 |
|------|------|----------|
| 1.7.4 | 2026-04-11 | 更正版本号变更规则（2.x.x -> 1.x.x） |
| 1.7.3 | 2026-04-11 | SKILL.md新增.pdca/目录初始化步骤和README.md内容规范 |
| 1.7.2 | 2026-04-11 | 添加版本发布检查清单、优化安装说明、修复SKILL.md版本号同步 |
| 1.7.1 | 2026-04-11 | 修复版本徽章链接、从仓库中移除.qoder和.trae文件夹 |
| 1.7.0 | 2026-04-11 | 模板分工明确化、参考文档添加按需加载触发条件、术语表核实 |
| 1.6.0 | 2026-04-11 | 修复审查问题：数据一致性、Mermaid规范、.gitignore完善、内容去重、目录结构统一 |
| 1.5.0 | 2026-04-11 | 添加.pdca/输出目录说明文件，补充跨平台时间获取命令 |
| 1.4.0 | 2026-04-11 | 优化问题编号规则：is -> issue |
| 1.3.0 | 2026-04-11 | 重构输出目录结构，创建issues文件夹 |
| 1.2.0 | 2026-04-10 | 基于SIPOC分析优化模板文件位置 |
| 1.1.0 | 2026-04-09 | 添加模板、检查清单、度量指标、FAQ |
| 1.0.1 | 2026-04-09 | 符合AgentSkills规范，添加中英文术语表 |
| 1.0.0 | 2026-04-09 | 初始版本 |

## 参考资料

- ISO 9000:2015 质量管理体系 基础和术语
- ISO 9001:2015 质量管理体系 要求
- 戴明《走出危机》
- 《质量管理学》
- [AgentSkills规范](https://agentskills.io/specification)

## 许可证

MIT License

## 作者

小翠 - 软件开发团队负责人

## 相关链接

- [GitHub仓库](https://github.com/normdist-ai/pdca)
- [AgentSkills规范](https://agentskills.io/specification)

---

**让PDCA成为您的持续改进利器！**
