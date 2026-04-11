# AgentSkills 规范检查清单

使用此检查清单确保技能符合 AgentSkills 规范。

主要参考：https://agentskills.io/specification

## 必需项检查

- [ ] 技能是一个包含 SKILL.md 的目录
- [ ] SKILL.md 以有效的 YAML frontmatter 开头
- [ ] Frontmatter 包含必需字段：
  - [ ] name
  - [ ] description

## name 字段规则

- [ ] 1-64 字符
- [ ] 仅包含小写字母、数字和连字符
- [ ] 不以连字符开头或结尾
- [ ] 不包含连续连字符
- [ ] 与父目录名称匹配

## description 字段规则

- [ ] 1-1024 字符
- [ ] 非空
- [ ] 描述技能的功能和何时使用

## Markdown 正文

- [ ] Frontmatter 后存在 Markdown 正文

## 最佳实践指导

- [ ] SKILL.md 保持在 ~500 行以内以提高上下文效率
- [ ] 使用渐进式披露：
  - [ ] 核心指令保留在 SKILL.md
  - [ ] 详细内容移至 references/
- [ ] 仅在确定性或重复工作时添加 scripts/
- [ ] 保持文件引用相对于技能根目录
- [ ] 保持引用浅层且易于从 SKILL.md 发现

## 可选 frontmatter 字段

- [ ] license（许可证）
- [ ] compatibility（兼容性）
- [ ] metadata（元数据）
- [ ] allowed-tools（实验性；支持因代理而异）

## 可移植性规则

- [ ] 避免特定于供应商的指令，除非用户要求
- [ ] 如果可能使用可移植路径，避免特定于代理的路径假设
- [ ] 避免依赖非标准工具而没有回退指导

## 验证命令

如果可用：
```bash
skills-ref validate ./<skill-name>
```

对于使用 skills CLI 的工作区中的发现检查：
```bash
npx skills list
```

## 示例结构

```
skill-name/
├── SKILL.md          # 必需：元数据 + 指令
├── scripts/          # 可选：可执行代码
├── references/       # 可选：文档
├── assets/           # 可选：模板、资源
└── ...               # 任何其他文件或目录
```

## 示例 Frontmatter

### 最小示例

```yaml
---
name: skill-name
description: 此技能的功能描述以及何时使用它。
---
```

### 包含可选字段的示例

```yaml
---
name: pdf-processing
description: 从PDF文件提取文本和表格，填写表单，合并文档。处理PDF文档或用户提到PDF、表单或文档提取时使用。
license: Apache-2.0
metadata:
  author: example-org
  version: "1.0"
---
```

## 常见错误

1. **name 字段使用引号**：规范要求不使用引号
2. **description 过于简短**：应包含功能和触发条件
3. **SKILL.md 过长**：应保持在 500 行以内
4. **缺少渐进式披露**：所有内容都在 SKILL.md 中
5. **name 与目录名不匹配**：必须与父目录名称一致
