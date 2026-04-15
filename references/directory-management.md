# PDCA工作目录管理指南

> 本文档详细说明PDCA技能运行时的目录结构、文件命名规范和使用流程。

---

## 📁 目录结构

### 输出目录（.pdca/）

PDCA技能运行时，会在**项目根目录**创建`.pdca/`文件夹，用于存储PDCA运行过程产生的**输出文件**。

```
项目根目录/
└── .pdca/
    ├── README.md              # 目录说明文件
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

### 过程规范目录（<技能安装目录>/pdca/）

模板和参考文档位于**技能安装目录**下：

```
<技能安装目录>/pdca/
├── templates/                 # 模板文件夹（过程规范）
│   ├── README.md              # 模板库总览说明
│   ├── issue-template.md      # 问题概述模板
│   ├── generic/               # 通用阶段模板
│   │   ├── plan-template.md   # Plan阶段通用模板
│   │   ├── do-template.md     # Do阶段通用模板
│   │   ├── check-template.md  # Check阶段通用模板
│   │   └── act-template.md    # Act阶段通用模板
│   └── scenarios/             # 场景专用模板
│       ├── bugfix/            # BUG修复场景
│       │   ├── template.md    # BUG修复PDCA模板
│       │   ├── example.md     # 使用示例
│       │   └── README.md      # 场景说明
│       ├── feature-dev/       # 功能开发场景
│       │   └── template.md    # 功能开发PDCA模板
│       ├── software-plan/     # 制定软件开发计划场景
│       │   └── template.md    # 制定计划PDCA模板
│       ├── code-review/       # 代码审查场景
│       │   └── template.md    # 代码审查PDCA模板
│       └── performance-opt/   # 性能优化场景
│           └── template.md    # 性能优化PDCA模板
├── references/                # 参考文档
└── assets/                    # 资产文件
```

---

## 📋 SIPOC分析

| 供方 (Supplier) | 输入 (Input) | 过程 (Process) | 输出 (Output) | 顾客 (Customer) |
|----------------|--------------|----------------|---------------|----------------|
| PDCA技能 | 用户需求 | PDCA方法论（含模板） | `.pdca/`文件夹中的过程文件 | 用户 |

**说明**：
- **过程规范**（模板文件）：位于`<技能安装目录>/pdca/templates/`
- **输出文件**（过程文件）：位于`.pdca/`文件夹中

---

## 📝 文件命名规范

### 问题文件夹命名

格式：`issue-yyyyMMdd-HHmmss`

- `issue`：Issue（问题）的完整单词
- `yyyyMMdd`：日期（年月日）
- `HHmmss`：时间（时分秒）
- 示例：`issue-20260409-143000`

### 过程文件命名

- Plan阶段：`plan-YYYYMMDD-HHMMSS.md`
- Do阶段：`do-YYYYMMDD-HHMMSS.md`
- Check阶段：`check-YYYYMMDD-HHMMSS.md`
- Act阶段：`act-YYYYMMDD-HHMMSS.md`

---

## 📊 问题索引列表

`issue-list.md`文件以表格形式记录所有问题：

| 问题ID | 问题描述 | 创建时间 | 状态 | 优先级 | 文件夹路径 |
|--------|----------|----------|------|--------|-----------|
| IS-001 | 问题描述 | 2026-04-09 14:30:00 | 进行中 | 高 | [issue-20260409-143000](./issues/issue-20260409-143000/) |

---

## 🔄 使用流程

### 初始化阶段（首次使用时）

1. 检查`.pdca/`目录是否存在，不存在则创建并生成`README.md`
2. 创建`issue-list.md`问题索引文件

### 每次启动PDCA循环

1. **获取当前时间**：使用 `Get-Date -Format "yyyyMMdd-HHmmss"` 获取实际当前时间
2. **创建问题文件夹**：`.pdca/issues/issue-yyyyMMdd-HHmmss/`
3. **创建问题概述**：在问题文件夹中创建 `README.md`
4. **更新问题索引**：在 `issue-list.md` 中添加新记录
5. **开始PDCA循环**：按阶段创建过程文件

### 重要提示

- ⚠️ **必须使用实际当前时间**，不能使用估算时间
- ⚠️ **时间格式必须为** `yyyyMMdd-HHmmss`
- ⚠️ **每个阶段完成后及时更新状态**

---

## 📄 README.md内容规范

`.pdca/README.md`是输出目录的说明文件，在首次初始化`.pdca/`目录时自动生成。

### 内容模板

```markdown
# .pdca/ 目录说明

本目录是 **PDCA技能** 的运行时输出文件夹，由代理在使用PDCA技能时自动创建和维护。

## 目录性质

- **类型**：输出目录（非版本控制内容）
- **创建者**：PDCA技能（基于ISO9000标准的PDCA循环方法论技能）
- **用途**：存储PDCA循环运行过程中产生的所有过程文件

## 目录结构

.pdca/
├── README.md                # 本说明文件
├── issue-list.md            # 问题索引列表
└── issues/                  # 问题文件夹
    └── issue-yyyyMMdd-HHmmss/  # 每个PDCA问题的独立文件夹
        ├── README.md        # 问题概述
        ├── plan/            # Plan阶段文件
        ├── do/              # Do阶段文件
        ├── check/           # Check阶段文件
        └── act/             # Act阶段文件

## 注意事项

1. 本目录中的文件为PDCA技能运行时自动生成，请勿手动修改索引文件
2. 本目录应添加到 `.gitignore`，不纳入版本控制
3. 过程规范（模板文件）位于技能安装目录下的 `templates/` 文件夹中，不在此输出目录内
```

---

## 💻 PowerShell示例

```powershell
# 初始化输出目录（首次使用时执行）
if (-not (Test-Path ".pdca")) {
    New-Item -Path ".pdca" -ItemType Directory -Force
    # 创建 README.md 说明文件
}

# 获取当前实际时间
$timestamp = Get-Date -Format "yyyyMMdd-HHmmss"

# 创建问题文件夹
$folderName = "issue-$timestamp"
New-Item -Path ".pdca\issues\$folderName" -ItemType Directory -Force
```

---

## 🔗 相关链接

- [PDCA技能说明](../SKILL.md)
- [模板库说明](../templates/README.md)
- [.pdca目录说明](../.pdca/README.md)

---

*最后更新: 2026-04-15*
