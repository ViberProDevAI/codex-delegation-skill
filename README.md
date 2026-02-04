# Codex Delegation Skill for Claude Code

> Delegate grunt work to codex CLI, preserve Claude's context for architecture

## 🎯 What This Does

This skill teaches Claude Code to automatically delegate **grunt work** (file searches, pattern matching, boilerplate) to the **codex CLI**, preserving Claude's precious context budget for **architectural decisions**.

## 📊 Impact

| Without Skill | With Skill |
|--------------|------------|
| 20 file searches = 20,000 tokens | 20 file searches = 2,000 codex tokens |
| Context exhausted after 10 tasks | 50+ tasks per session |
| No room for architecture work | Deep architectural analysis possible |
| **10x context multiplier** | **50x context multiplier** |

## 🚀 Installation

### Prerequisites

1. **codex CLI** must be installed:
```bash
npm install -g @openai/codex-cli
codex login
```

2. Verify codex works:
```bash
codex exec "list files in current directory"
```

### Install Skill

```bash
# Create skills directory if it doesn't exist
mkdir -p ~/.claude/skills/codex-delegation

# Copy skill file
cp SKILL.md ~/.claude/skills/codex-delegation/

# Restart Claude Code
```

That's it! The skill will auto-load in every session.

## 🎓 How It Works

Once installed, Claude will automatically follow this decision tree:

```
New task arrives
    │
    ├─ Is it grunt work? (search, count, list, pattern)
    │   └─ YES → Use codex CLI ✅
    │
    ├─ Does it require architectural judgment?
    │   └─ YES → Claude does it ✅
    │
    └─ Mixed task?
        └─ codex prep → Claude analysis ✅
```

### Examples

**Grunt work (codex):**
```bash
codex exec "find all files over 500 lines"
codex exec "count TODO comments"
codex exec "list all singleton usages"
```

**Architectural work (Claude):**
- Design decisions (SSOT, dependency injection)
- Critical business logic review
- State management architecture
- Security/performance trade-offs

**Mixed (codex prep + Claude decides):**
- Codex: "Found 20 large files"
- Claude: "ArgusDecisionEngine should split into 7 services"

## 🧪 Testing

This skill was created using **TDD methodology** with pressure scenarios:

- ✅ Time pressure resistance
- ✅ "Quick task" rationalization resistance
- ✅ Mixed task delegation
- ✅ Architectural work stays with Claude

## 📖 What's Inside

The skill includes:

- **Decision flowchart** - When to use codex vs Claude
- **Quick reference table** - Common tasks and tools
- **Red flags list** - Detect when you're rationalizing
- **Rationalization table** - Counter common excuses
- **The Iron Law** - "Grunt work goes to codex, no exceptions"

## 🤝 Contributing

Found a rationalization loophole? Encountered a new pressure scenario? PRs welcome!

## 📄 License

[Unlicense](LICENSE) - Public Domain

## 🙏 Credits

Created using the **superpowers:writing-skills** methodology - TDD for documentation.
