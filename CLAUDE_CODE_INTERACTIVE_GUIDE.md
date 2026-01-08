# Claude Code Interactive Guide
> A hands-on tutorial to master Claude Code - learn by doing!

*Based on tips from Boris Cherny (Claude Code creator), Anthropic's official guides, DeepLearning.AI, and the developer community.*

---

## Table of Contents
1. [Level 1: Essential Commands](#level-1-essential-commands)
2. [Level 2: Workflow Boosters](#level-2-workflow-boosters)
3. [Level 3: Plan Mode Mastery](#level-3-plan-mode-mastery)
4. [Level 4: Memory & Context](#level-4-memory--context)
5. [Level 5: Power User Techniques](#level-5-power-user-techniques)
6. [Level 6: Advanced Orchestration](#level-6-advanced-orchestration)

---

## Level 1: Essential Commands

### Exercise 1.1: The Bang Prefix (!)
Instead of asking Claude to run commands, use `!` to execute bash instantly.

**Try it now** - Type these in your Claude Code session:
```
!pwd
!ls -la
!git status
```

> **Pro tip from Ado (Anthropic)**: "Don't waste tokens asking Claude to run commands. The output goes straight into context with no model processing."

### Exercise 1.2: Clearing Context
Start fresh when switching tasks to save tokens and avoid confusion.

**Try it now**:
```
/clear
```

> **Pro tip from Builder.io**: "Every time you start something new, clear the chat. You don't need all that history eating your tokens."

### Exercise 1.3: Getting Help
**Try it now**:
```
/help
```
This shows all available slash commands.

---

## Level 2: Workflow Boosters

### Exercise 2.1: Ask Claude to Explain the Codebase
Before making changes, understand what you're working with.

**Try it now** - Ask me:
```
"Explain this codebase to me - what files are here and what's the structure?"
```

### Exercise 2.2: Screenshot Pasting
Claude Code can see and understand images!

**Try it now** (macOS):
1. Press `Cmd+Ctrl+Shift+4` to screenshot to clipboard
2. Press `Ctrl+V` to paste into Claude Code
3. Ask "What do you see in this screenshot?"

### Exercise 2.3: Session Management
Name your sessions for easy retrieval later.

**Try it now**:
```
/sessions
```
See your past sessions. You can resume any of them!

---

## Level 3: Plan Mode Mastery

### Exercise 3.1: Entering Plan Mode
Plan mode lets you collaborate on a plan BEFORE Claude writes any code.

**Try it now**:
- Press `Shift+Tab` twice to toggle into Plan mode, OR
- Press `Escape` to open the menu and select Plan mode

> **Pro tip from Boris Cherny**: "Most sessions start in Plan mode. If the goal is to write a PR, go back and forth until you like the plan. Then switch into auto-accept mode and Claude can usually 1-shot it."

### Exercise 3.2: Planning a Feature
**Try it now** in Plan mode:
```
"I want to add a simple 'Hello World' Python script to this repo. What's your plan?"
```

Review the plan, give feedback, then switch to Act mode to execute.

---

## Level 4: Memory & Context

### Exercise 4.1: Understanding CLAUDE.md
Claude automatically reads `CLAUDE.md` files in your project root.

**Try it now** - Ask me:
```
"Create a CLAUDE.md file for this project with basic coding guidelines"
```

> **Pro tip from Boris**: "My team shares a single CLAUDE.md, checked into git. Anytime we see Claude do something incorrectly, we add it to the CLAUDE.md."

### Exercise 4.2: Memory Commands
See what Claude remembers about your project:

**Try it now**:
```
/memory
```

---

## Level 5: Power User Techniques

### Exercise 5.1: Deep Thinking with Magic Words
For complex problems, trigger deeper analysis.

**Try it now** - Include "ultrathink" in your prompt:
```
"Ultrathink: What are the best practices for structuring a Python project?"
```

### Exercise 5.2: Verification Loops
The #1 tip from the Claude Code creator:

> **Boris Cherny**: "Give Claude a way to verify its work. If Claude has that feedback loop, it will 2-3x the quality of the final result."

**Try it now**:
```
"Write a function that checks if a number is prime, then write tests for it and run them"
```

Watch Claude write code, create tests, run them, and fix any failures!

### Exercise 5.3: Multi-File Operations
**Try it now**:
```
"Find all Python files in this directory and list them"
```

Then try:
```
"Add a docstring to every function that doesn't have one"
```

---

## Level 6: Advanced Orchestration

### Exercise 6.1: Custom Slash Commands
Create reusable prompts in `.claude/commands/`.

**Try it now** - Ask me:
```
"Create a custom slash command called /explain that explains any file I give it"
```

### Exercise 6.2: Git Workflow Automation
**Try it now**:
```
"Create a commit with a good message for any changes we've made"
```

Or ask about PRs:
```
"What would a PR look like for the changes in this session?"
```

### Exercise 6.3: Parallel Work
> **Pro tip from Boris**: He runs "5 Claudes in parallel in terminal, numbered 1-5"

You can open multiple terminal tabs and run separate Claude Code sessions for different tasks!

---

## Quick Reference Card

| Command | What it does |
|---------|-------------|
| `!command` | Execute bash instantly |
| `/clear` | Clear conversation context |
| `/help` | Show all commands |
| `/sessions` | List past sessions |
| `/memory` | Show project memory |
| `Shift+Tab` x2 | Toggle Plan mode |
| `Escape` | Open command menu |
| `Ctrl+C` | Cancel current operation |

## Magic Prompting Words
- **"ultrathink"** - Triggers deeper analysis
- **"step by step"** - Encourages methodical approach
- **"verify your work"** - Activates self-checking

---

## Sources & Further Learning

- [How the Creator of Claude Code Uses It](https://twitter-thread.com/t/2007179832300581177) - Boris Cherny's Twitter thread
- [Official Quickstart Guide](https://code.claude.com/docs/en/quickstart)
- [40+ Claude Code Tips Repository](https://github.com/ykdojo/claude-code-tips)
- [The Ultimate Claude Code Tips Collection](https://dev.to/damogallagher/the-ultimate-claude-code-tips-collection-advent-of-claude-2025-5b73)
- [Anthropic's Best Practices Guide](https://www.anthropic.com/engineering/claude-code-best-practices)
- [DeepLearning.AI Course](https://learn.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant)
- [Builder.io Claude Code Tips](https://www.builder.io/blog/claude-code)
- [Appwrite Tips & Tricks](https://appwrite.io/blog/post/claude-code-tips-tricks)
- [20 Tips to Master Claude Code](https://creatoreconomy.so/p/20-tips-to-master-claude-code-in-35-min-build-an-app)

---

*Now let's start the interactive exercises! Go back to your Claude Code session and we'll do them together.*
