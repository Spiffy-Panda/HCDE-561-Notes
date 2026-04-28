# Vocabulary Primer — Core Concepts for AI Practice

A working glossary you'll use for the rest of this quarter. Keep this handy. The terms here travel across tools — Claude Code, ChatGPT, Custom GPTs, Claude Projects, Gemini, UW Purple — but the *names* differ. We'll use the canonical names and translate as needed.

---

## Markdown

**One-line definition:** Plain text with light formatting marks (pound signs for headings, asterisks for emphasis, dashes for lists).

**Why it matters for AI work:** Almost every file you'll write for AI consumption is markdown. Master instructions files, personal context files, skill files, prompt templates — all markdown. AI models read it more fluently than any other format because the structure is semantically obvious to them.

**What you need to know:** Headings (`#`, `##`, `###`), bold (`**bold**`), italic (`*italic*`), bulleted lists (`-`), numbered lists (`1.`), links (`[text](url)`), code blocks (triple backticks), and blockquotes (`>`). That's the working set. See the [Markdown Primer](markdown-primer.md) for the full ramp.

---

## Master Instructions

**One-line definition:** A single document that tells an AI everything it needs to know to behave the way you want, every time, in a given project or context.

**Why it matters:** This file is the foundation. It's where your rules, references, format preferences, identity framing, and workflow patterns live. A well-written master instructions file is what separates "AI gives me generic output" from "AI gives me output that's specific to me, my project, and how I work."

**What goes in it:**

- **Identity / role.** Who the AI is acting as in this project.
- **Context.** What this project is, who's involved.
- **References.** Pointers to other files (`See also: ./about-me/`, `See also: ./project/`).
- **Rules.** Always do X. Never do Y.
- **Workflows.** When the user says A, follow these steps.
- **Format preferences.** How outputs should be shaped (length, structure, tone).

**What does NOT go in it:**

- Your personal background → goes in `about-me/`
- Project-specific research and context → goes in `project/`
- Skills or templates → go in `library/`
- Actual deliverables → go in `work/`

**Where master instructions lives across products:**

| Tool | Where | Notes |
|---|---|---|
| Claude Code | `CLAUDE.md` in project root + `~/.claude/CLAUDE.md` for global | Read automatically every session |
| OpenAI Codex | `AGENTS.md` | Read automatically |
| Cursor | `.cursorrules` | Read automatically |
| Gemini CLI | `GEMINI.md` | Read automatically |
| Claude Project | "Project instructions" field at top of project | Applied to every chat in that project |
| Custom GPT | "Instructions" field in GPT config | Applied to every conversation with that GPT |
| ChatGPT or Claude Chat (no project) | Whatever you paste at the top of the conversation | Lost when conversation ends |
| UW Purple custom agent | System prompt field | UW-hosted, applied per agent |

**The portability principle:** The same well-written master instructions content works in any of these. The structure is portable. What changes is *how* the AI loads it and whether it persists across sessions.

**One-line takeaway:** Master instructions is your safety/compliance layer made explicit. It's where your judgment gets encoded.

---

## Skills

**One-line definition:** A reusable, named capability you give an AI — packaged instructions, examples, and (sometimes) small bits of code or templates — that the AI can pick up when the task calls for it.

**Why it matters:** Skills are how you scale your judgment. Once you've figured out the right way to do something — write a stakeholder update, clean up meeting notes, run a competitive analysis — you can write it down once as a skill, and the AI will use that pattern every time you ask for it. You're encoding expertise into a portable form.

**What a skill looks like:** A folder with a `SKILL.md` file. The file has front matter (name, description) and instructions for the AI. Optionally, the folder includes templates, examples, or scripts the skill uses.

```
my-skill/
├── SKILL.md
├── examples/
│   └── good-output.md
└── templates/
    └── starter.md
```

**The trigger:** The AI loads a skill when the task at hand matches the skill's *description* (the field in front matter). If the description is vague, the skill won't trigger when it should. If the description is sharp, the skill loads automatically. Writing good descriptions is half of writing a good skill.

**Where skills live across products:**

| Tool | Where | Notes |
|---|---|---|
| Claude Code | `~/.claude/skills/` (user) or `.claude/skills/` (project) | Folders with SKILL.md files |
| Anthropic | Pre-built skills (PowerPoint, Excel, PDF, Word) | Available in Claude Code and Claude.ai |
| Custom GPT | "Knowledge" files + "Instructions" | Less structured; you upload reference files and write instructions to use them |
| Claude Project | Knowledge base + project instructions | Same idea as Custom GPT |
| Chat-with-paste | Manual — paste skill instructions when needed | Loses the auto-trigger |

**One-line takeaway:** Skills are how you write down once and apply forever. They're the seed of functional replacement — packaging up your judgment so AI can apply it without you in the loop.

---

## Agents and Subagents

**One-line definition:** An *agent* is an AI that takes actions in a loop — read, decide, act, observe, repeat — toward a goal. A *subagent* is an agent spawned by another agent to handle a specific subtask, with its own context and its own tools.

**Why it matters:** Most of the AI work you've done so far is *not* agentic. You ask a question, the AI answers. That's a chat. An agent has a goal and works toward it across many steps, often with tool access (reading files, running commands, browsing the web). Once you're working in Claude Code, ChatGPT's agent mode, or Cursor's agent mode, you're working with an agent — even if you don't think of it that way.

**The key idea behind subagents: isolation.** A subagent has its own focused context — separate from the parent — and only reports back when its work is done. The parent doesn't see the subagent's intermediate steps, exploratory thinking, or tool calls. It just gets the final result.

This matters because:

- **Context windows are finite.** A complex task can fill the parent agent's context with intermediate noise. Subagents keep that noise isolated.
- **Specialization helps.** A subagent dedicated to one task (research, code review, data extraction) often does it better than a general agent juggling everything.
- **Parallelism becomes possible.** Multiple subagents can work on different subtasks simultaneously.

**What a subagent looks like in practice:** In Claude Code, you can define subagents in `.claude/agents/` (project-level) or `~/.claude/agents/` (user-level). Each has its own system prompt, tool permissions, and description. The parent agent reads the description and decides whether to delegate.

**Where agents and subagents live across products:**

| Tool | Agent capability | Subagent support |
|---|---|---|
| Claude Code | Full agent mode + Agent Teams (subagents) | Yes — define in `.claude/agents/` |
| Cursor | Agent mode | Limited — single agent |
| ChatGPT (agent mode) | Agent mode | Limited — single agent |
| OpenAI Codex | Agent mode | Yes — Codex CLI supports agent orchestration |
| Custom GPT or chat | Conversational, not agentic | No |

**Subagents in this course:** We're not teaching you to architect multi-agent systems this quarter — that's a deeper engineering topic. But you'll encounter the language, and sometimes the right move when working in an agentic harness is to delegate a subtask to a subagent and let it think on its own.

**One-line takeaway:** Agents act in loops toward goals. Subagents are workers spawned with their own context. The cliff between "AI as chat" and "AI as agent" is real — and it's where the Hutchins concerns from Week 4 start to apply.

---

## How these four concepts work together

A complete AI knowledge system uses all four:

- **Markdown** is the format you write everything in.
- **Master instructions** is the index file that tells the AI what's in your system, what rules apply, and where to look.
- **Skills** are the named capabilities your AI can pick up — your encoded judgment, available on demand.
- **Agents and subagents** are the runtime — the thing actually executing the work, in a loop, with access to tools and the file structure you've built.

You'll see all four operating in the Hour 2 live demo. Watch for them.

---

## Translation table — what to call things in different tools

A handy reference if you're switching between tools and the names confuse you:

| Concept | Claude Code | OpenAI / Codex | Cursor | Gemini | Claude Project | Custom GPT |
|---|---|---|---|---|---|---|
| Master instructions | `CLAUDE.md` | `AGENTS.md` | `.cursorrules` | `GEMINI.md` | Project instructions | Instructions field |
| Skills | `.claude/skills/` | (limited) | (limited) | (limited) | Knowledge + instructions | Knowledge + instructions |
| Subagents | `.claude/agents/` | Codex agent orchestration | (single agent) | Subagent support emerging | (no subagents) | (no subagents) |
| Personal context | Referenced from `CLAUDE.md` | Referenced from `AGENTS.md` | Referenced from rules | Referenced from `GEMINI.md` | Knowledge file | Knowledge file |

The point isn't to memorize this. It's to recognize that **the concepts are universal — the names are local**. When you read documentation for any of these tools, you'll know what they're talking about even when the names are different.
