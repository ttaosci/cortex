# Cortex

Cortex helps agents track project issues, tasks, and changes with minimal overhead.

## Usage
```bash
git clone https://github.com/ttaosci/cortex.git

# <skill_dir>
# Codex: .agents/skills
# Claude: .claude/skills
mkdir -p <project_root>/<skill_dir>
cp -r cortex/cortex <project_root>/<skill_dir>/cortex
# Cortex stores project-local issues and change history here
export CORTEX_HOME=<project_root>/cortex
# In Codex or Claude Code
> $cortex Write me a script that calculates tips.
```
