# PDCA Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skill Type](https://img.shields.io/badge/Type-SKILL-blue.svg)](https://agentskills.io)
[![Version](https://img.shields.io/badge/Version-1.7.6-green.svg)](https://github.com/normdist-ai/pdca)

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

### Installation Instructions

When a user requests to install this skill (e.g., `Install https://github.com/normdist-ai/pdca`), follow these steps:

1. **Clone the repository** (must use git clone, do not download ZIP):
   ```bash
   git clone https://github.com/normdist-ai/pdca.git
   ```

2. **Detect current IDE**: Check for IDE config folders (e.g., `.trae/`, `.cursor/`, `.vscode/`, etc.)

3. **Copy to skills directory**: Copy the cloned `pdca` folder to the IDE's skills directory, ensuring the final path is `{skills_dir}/pdca/`

### IDE Skills Directories

| IDE | Skills Directory | Detection Flag |
|-----|------------------|----------------|
| Trae | `.trae/skills/pdca` | `.trae/` folder exists |
| Cursor | `.cursor/skills/pdca` | `.cursor/` folder exists |
| VS Code | `.vscode/skills/pdca` | `.vscode/` folder exists |
| OpenCode | `~/.config/opencode/skills/pdca` | Linux/macOS default path |
| Lingma | `.lingma/skills/pdca` | `.lingma/` folder exists |
| Windsurf | `.windsurf/skills/pdca` | `.windsurf/` folder exists |
| Claude Code | `~/.config/claude-code/skills/pdca` | Claude Code CLI environment |

### Installation Examples

```bash
# Clone the repository
git clone https://github.com/normdist-ai/pdca.git

# Copy to Trae IDE (example)
cp -r pdca .trae/skills/

# Or copy to Cursor IDE
cp -r pdca .cursor/skills/

# Windows PowerShell example
Copy-Item -Recurse pdca .trae\skills\
```

### Installation Verification

After installation, the skills directory structure should be:
```
{skills_dir}/pdca/
├── SKILL.md           # Skill definition file (required)
├── assets/            # Asset files
├── references/        # Reference documents
└── templates/         # Template files
```

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
| 1.7.6 | 2026-04-15 | Optimized SKILL.md structure, streamlined core content, enhanced navigation and interaction guidance |
| 1.7.5 | 2026-04-11 | Corrected version numbering convention (2.x.x -> 1.x.x) |
| 1.7.4 | 2026-04-11 | Added .pdca/ directory initialization step and README.md content specification to SKILL.md |
| 1.7.2 | 2026-04-11 | Added version release checklist, optimized installation instructions, fixed SKILL.md version sync |
| 1.7.1 | 2026-04-11 | Fixed version badge link, removed .qoder and .trae from repository |
| 1.7.0 | 2026-04-11 | Clarified template division, added on-demand loading triggers for reference docs, verified glossary |
| 1.6.0 | 2026-04-11 | Fixed review issues: data consistency, Mermaid compliance, .gitignore improvements, content deduplication, unified directory structure |
| 1.5.0 | 2026-04-11 | Added .pdca/ output directory README, added cross-platform time retrieval commands |
| 1.4.0 | 2026-04-11 | Optimized issue numbering: is -> issue |
| 1.3.0 | 2026-04-11 | Restructured output directory, created issues folder |
| 1.2.0 | 2026-04-10 | Optimized template file locations based on SIPOC analysis |
| 1.1.0 | 2026-04-09 | Added templates, checklists, metrics, FAQ |
| 1.0.1 | 2026-04-09 | Compliant with AgentSkills specification, added bilingual glossary |
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
