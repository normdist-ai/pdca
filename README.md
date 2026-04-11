# PDCA Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skill Type](https://img.shields.io/badge/Type-SKILL-blue.svg)](https://agentskills.io)
[![Version](https://img.shields.io/badge/Version-2.7.1-green.svg)](https://github.com/normdist-ai/pdca)

[中文文档](README.zh.md)

A PDCA cycle methodology skill based on ISO9000 standards, guiding agents to work systematically through Plan, Do, Check, and Act phases to help users achieve continuous improvement.

## Overview

This skill follows the Agent Skills open standard, fully supports OpenClaw platform, and is compatible with mainstream IDEs like Trae, Cursor, VS Code, Claude Code, etc. When triggered, the agent reads the skill instructions and works through the four PDCA phases systematically to help users achieve continuous improvement.

## Compatibility

### Supported IDEs

This skill is fully compatible with the following IDEs:

| IDE | Support Status | Skills Directory |
|------|----------------|------------------|
| Trae | ✅ Fully Supported | `.trae/skills/` |
| Cursor | ✅ Fully Supported | `.cursor/skills/` |
| VS Code | ✅ Fully Supported | `.vscode/skills/` |
| OpenCode | ✅ Fully Supported | `~/.config/opencode/skills/` |
| Lingma | ✅ Fully Supported | `.lingma/skills/` |
| Windsurf | ✅ Fully Supported | `.windsurf/skills/` |
| Claude Code | ✅ Fully Supported | `~/.config/claude-code/skills/` |

### Supported Agent Platforms

This skill runs on the following Agent platforms:

| Platform | Support Status | Description |
|----------|----------------|-------------|
| OpenClaw | ✅ Fully Supported | Recommended Platform - Open-source self-hosted Agent platform with perfect progressive disclosure support |
| Claude Code | ✅ Fully Supported | Anthropic's official CLI tool |
| Other Agent Frameworks | ✅ Compatible | Any framework supporting SKILL.md specification |

## Technical Features

- ✅ **SKILL.md v3.0 Specification**: Fully compliant with the latest standard
- ✅ **Progressive Disclosure**: Metadata → Instructions → References, reducing token consumption
- ✅ **Cross-Platform**: Windows (PowerShell) + Linux/macOS (Bash)
- ✅ **Standardized Output**: Unified issue folder structure for easy tracing and management
- ✅ **Complete Documentation**: Theory foundation, complete examples, checklists, metrics, FAQ, glossary

## Supported Methodology Tools

| Tool | Purpose | Application Phase |
|------|---------|-------------------|
| **SMART** | Goal setting (Specific, Measurable, Achievable, Relevant, Time-bound) | Plan |
| **WBS** | Work Breakdown Structure (milestones, work packages) | Plan |
| **SIPOC** | Process analysis (Suppliers, Inputs, Process, Outputs, Customers) | Plan/Do |
| **5WHY** | Root cause analysis (continuous "why" questioning) | Check |
| **SWOT** | Risk identification (Strengths, Weaknesses, Opportunities, Threats) | Plan |
| **MECE** | Classification (Mutually Exclusive, Collectively Exhaustive) | Plan/Check |

## Installation

### Option 1: Clone Repository

```bash
# Clone the repository
git clone https://github.com/normdist-ai/pdca.git

# Copy to your IDE's skills directory
cp -r pdca .trae/skills/
```

### Option 2: IDE-Specific Paths

| IDE | Skills Directory |
|-----|------------------|
| Trae | `.trae/skills/pdca` |
| Cursor | `.cursor/skills/pdca` |
| VS Code | `.vscode/skills/pdca` |
| OpenCode | `~/.config/opencode/skills/pdca` |
| Lingma | `.lingma/skills/pdca` |
| Windsurf | `.windsurf/skills/pdca` |
| Claude Code | `~/.config/claude-code/skills/pdca` |

## Usage

### Trigger Phrases

The skill is automatically triggered when you mention:

- `PDCA`, `PDCA cycle`, `Deming cycle`
- `continuous improvement`, `quality management`
- `project planning`, `problem solving`, `process improvement`

### Example Interaction

```
User: I want to use PDCA method to improve the code review process

Agent: I'll help you start the PDCA cycle to improve the code review process.
       
       Plan Phase
       Let's first clarify the goals...
       
       [Execute planning phase activities]
       
       ✓ Goals determined, moving to implementation phase...
```

```
User: /pdca optimize project management process

Agent: [Start PDCA cycle, create issue folder, record process]
```

## Project Structure

```
pdca/
├── SKILL.md                   # Skill definition (Agent instructions)
├── README.md                  # Project documentation
├── LICENSE                    # MIT License
├── assets/                    # Asset files
│   ├── agentskills-checklist.md
│   ├── skill-description-guidelines.md
│   └── skill-usage-checklist.md
├── references/                # Reference documents
│   ├── checklists.md          # Checklists
│   ├── example.md             # Complete example
│   ├── faq.md                 # FAQ
│   ├── glossary.md            # Glossary
│   ├── metrics.md             # Metrics
│   ├── templates.md           # Practical templates
│   └── theory.md              # Theory foundation
└── templates/                 # Template files
    ├── act-template.md        # Act phase template
    ├── check-template.md      # Check phase template
    ├── do-template.md         # Do phase template
    ├── issue-template.md      # Issue overview template
    └── plan-template.md       # Plan phase template
```

## How It Works

1. **Trigger**: Agent detects the need for PDCA methodology support
2. **Load**: Agent reads SKILL.md for detailed instructions
3. **Execute**: Work through Plan → Do → Check → Act phases
4. **Output**: Create `.pdca/` folder in project root to record the complete process

## Four-Phase Methodology

| Phase | Description | Core Objective | Key Activities | Main Outputs |
|-------|-------------|----------------|----------------|--------------|
| **Plan** | Planning | Establish objectives and processes | SMART goal setting, WBS breakdown, SIPOC analysis | Goal statement, WBS, flowcharts |
| **Do** | Implementation | Execute the plan | Task execution, progress tracking, documentation | Execution records, progress reports, issue lists |
| **Check** | Checking | Monitor and measure results | Result verification, deviation analysis, 5WHY root cause analysis | Check reports, deviation analysis, root cause records |
| **Act** | Acting | Continuously improve performance | Lessons learned, standardization, improvement measures | Lessons learned, standardized documents, improvement plans |

## Application Scenarios

| Scenario | Plan | Do | Check | Act |
|----------|------|-----|-------|-----|
| **Project Management** | Define charter | Execute & monitor | Phase review | Summarize & archive |
| **Problem Solving** | Define countermeasures | Implement improvements | Verify root cause | Standardize prevention |
| **Process Improvement** | Identify opportunities | Implement new process | Evaluate performance | Solidify optimization |

## Important Notes

1. **Closed-loop Thinking**: Must complete the full PDCA cycle, not just the first two phases
2. **Data-driven**: The Check phase must be based on objective data
3. **Continuous Improvement**: The Act phase should set higher goals for the next cycle

## Version History

| Version | Date | Major Updates |
|---------|------|---------------|
| 2.7.0 | 2026-04-11 | Clarified template division, added on-demand loading triggers for reference docs, verified glossary |
| 2.6.0 | 2026-04-11 | Fixed review issues: data consistency, Mermaid compliance, .gitignore improvements, content deduplication, unified directory structure |
| 2.5.0 | 2026-04-11 | Added .pdca/ output directory README, added cross-platform time retrieval commands |
| 2.4.0 | 2026-04-11 | Optimized issue numbering: is -> issue |
| 2.3.0 | 2026-04-11 | Restructured output directory, created issues folder |
| 2.2.0 | 2026-04-10 | Optimized template file locations based on SIPOC analysis |
| 2.1.0 | 2026-04-09 | Added templates, checklists, metrics, FAQ |
| 2.0.0 | 2026-04-09 | Compliant with AgentSkills specification, added bilingual glossary |
| 1.0.0 | 2026-04-09 | Initial version |

## References

- ISO 9000:2015 Quality management systems - Fundamentals and vocabulary
- ISO 9001:2015 Quality management systems - Requirements
- W. Edwards Deming "Out of the Crisis"
- "Quality Management"
- [AgentSkills Specification](https://agentskills.io/specification)

## License

MIT License

## Author

Xiaocui - Software Development Team Lead

## Related Links

- [GitHub Repository](https://github.com/normdist-ai/pdca)
- [AgentSkills Specification](https://agentskills.io/specification)

---

**Make PDCA your tool for continuous improvement!**
