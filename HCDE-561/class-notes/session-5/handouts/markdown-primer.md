# A Quick Markdown Primer for AI Practice

**Why this is here:** AI tools read and write markdown more fluently than any other format. The major instructions files you'll work with — `CLAUDE.md`, `AGENTS.md`, `GEMINI.md`, system prompts, Custom GPT instructions — are markdown. So are most skill files, most prompt templates, and most documentation conventions in the AI world. You don't need to be fluent in markdown to do the work in this course. You do need to recognize the major patterns, write basic structure, and not be intimidated.

**How long this takes:** ~10 minutes to read. Maybe 20 minutes to write your first markdown file from scratch. After that, it's automatic.

---

## What markdown is

Markdown is plain text with light formatting marks. You write text mostly the way you'd type it into a normal document, plus a few special characters that indicate structure: pound signs for headings, asterisks for emphasis, dashes for lists, and so on.

It's not a complicated language. The cheat sheet that follows is the *whole* working set for almost every situation. There are obscure markdown features, but you can ignore them.

The reason markdown is everywhere in the AI world is that it's:

- **Human-readable.** You can read a `.md` file in any text editor and immediately see what it says.
- **Machine-readable.** AI models parse markdown structure cleanly — they understand that `## Voice` is a section heading, that `- never use leverage` is a list item, that `**this**` is emphasized.
- **Lightweight.** No fonts, no colors, no proprietary formats. Just text and a handful of symbols.
- **Composable.** You can paste markdown into any AI tool and it works. You can also render it to HTML, PDF, or formatted documents when you need to.

When you write a personal context file, a skill, a master instructions file, or a project brief for AI use — you'll be writing markdown.

---

## The cheat sheet

This covers ~95% of what you'll write.

### Headings

Pound signs at the start of a line. The number of pound signs is the heading level.

```markdown
# Top-level heading (H1)

## Section heading (H2)

### Subsection (H3)

#### Sub-subsection (H4)
```

Conventions:

- One H1 per file. It's the title.
- Use H2 for major sections, H3 for subsections, H4 sparingly.
- Leave a blank line before and after a heading.

### Bold and italic

Wrap text in asterisks.

```markdown
This is **bold text**. This is *italic text*. This is ***bold and italic***.
```

Conventions:

- Use bold for keywords or emphasized terms within a sentence.
- Use italics for titles of works, foreign phrases, or genuine emphasis. Don't overuse.

### Lists

Bulleted lists use dashes:

```markdown
- First item
- Second item
- Third item
```

Numbered lists use numbers (you can use `1.` for every item — markdown will renumber automatically):

```markdown
1. First step
2. Second step
3. Third step
```

Nested lists indent two or four spaces:

```markdown
- Top-level item
  - Sub-item
  - Another sub-item
- Another top-level item
```

### Links

Square brackets for the link text, parentheses for the URL.

```markdown
See the [Anthropic docs](https://docs.anthropic.com) for more.
```

### Inline code and code blocks

Single backticks for inline code (a function name, a filename, a snippet):

```markdown
The file is called `CLAUDE.md` and lives in the project root.
```

Triple backticks for multi-line code blocks. You can specify a language for syntax highlighting:

````markdown
```python
def hello():
    print("hi")
```
````

In AI work, you'll mostly use code blocks for examples of input or output, or for any structured data the AI should read literally.

### Blockquotes

Greater-than sign at the start of a line.

```markdown
> A blockquote is useful for quoted text, examples, or
> sections you want to set off visually.
```

In a personal context file, blockquotes are great for **voice samples** — sentences captured verbatim that show how you actually talk:

```markdown
> "Let's not lead with the recommendation. Lead with what surprised us."
```

### Horizontal rules

Three dashes on their own line. Used to separate major sections.

```markdown
---
```

### Tables

Tables use pipes and dashes. They're slightly fiddly but worth knowing.

```markdown
| Tool | Where master instructions live |
|---|---|
| Claude Code | CLAUDE.md in project root |
| Custom GPT | Instructions field |
| Claude Project | Project instructions |
```

You don't need to align the pipes — markdown will figure it out. The dashes in the second row tell markdown "this is a table." You can omit tables entirely and use lists instead if you find them awkward.

---

## What's worth knowing beyond the basics

A few patterns that come up specifically in AI-related markdown:

### Front matter

Some markdown files (especially skill files) start with a block of metadata at the top, set off by triple-dashes. This is called "front matter" and is YAML-formatted:

```markdown
---
name: stakeholder-update-writer
description: Drafts stakeholder updates from raw meeting notes and project status
---

# Stakeholder Update Writer

Instructions go here...
```

The AI reads the front matter for metadata about the file. You'll see this in skill files. You can copy the pattern when writing your own.

### Comments

HTML-style comments work in markdown and are invisible when rendered:

```markdown
<!-- This is a comment that won't appear in the rendered output. -->
```

Useful for leaving yourself notes inside a file.

### Linking between files

You can link to other markdown files in the same directory or project using relative paths:

```markdown
See also: [my voice profile](my-voice.md) and [my collaborators](my-collaborators.md).
```

In Claude Code and similar tools, the AI follows these references and reads the linked files.

---

## What to ignore

Things that exist in markdown but you probably won't use:

- **Inline HTML.** Markdown allows raw HTML. You almost never need it for AI work.
- **Reference-style links.** A more verbose way of writing links. The simple `[text](url)` style is fine.
- **Definition lists, footnotes, abbreviations.** Niche features. Skip.
- **Strikethrough** (`~~text~~`) and **task lists** (`- [ ] item`). Useful in some contexts (GitHub, Notion), but not load-bearing for AI work.

If something in a markdown file looks fancy and you don't recognize it, just trust that it works and move on.

---

## How to write a markdown file from scratch

You don't need a special tool. Markdown is plain text. You can write it in:

- **Any text editor** — TextEdit (Mac, in plain text mode), Notepad (Windows), VS Code, Sublime Text, anything
- **A code editor** — VS Code is the standard recommendation; it renders markdown previews and has good keyboard shortcuts
- **Obsidian, Bear, iA Writer, Typora** — note-taking apps designed around markdown
- **Notion** (with markdown export), Google Docs (with copy-paste, mostly works), Word (works but adds noise)

For files you'll use with AI tools, save them with a `.md` extension (`my-file.md`). The extension matters — some tools look for it specifically.

**Tip:** When you're writing a markdown file you'll feed to AI, preview it in a renderer once before you save. Quick way: paste it into [dillinger.io](https://dillinger.io) or any online markdown previewer. If the structure looks right rendered, the AI is reading it the way you intended.

---

## Markdown for AI files specifically — patterns to reach for

A few conventions that are common in AI-related markdown files:

**Use headings as semantic structure.** The AI uses your headings to understand the structure of the document. A file with clear `## Voice` and `## Anti-patterns` and `## Collaborators` sections is much more useful than the same content as one long paragraph.

**Use bullets for lists of discrete items.** Names, tools, rules, items. Don't use bullets for prose — paragraphs read better.

**Use blockquotes for voice samples.** When you want the AI to capture how you actually talk, put a verbatim quote in a blockquote. This is a strong signal: "this is how I sound, match it."

**Use bold for keywords inside paragraphs.** Helps the AI (and a human reader) skim. Don't over-bold; if everything is bold, nothing is.

**Use file references when files are related.** `See also: ./project/brief.md` — most AI tools will follow these. It saves you from repeating content across files.

**Keep files focused.** One concept per file. A long, sprawling document is harder for both humans and AI to use than several short focused ones.

---

## Common mistakes

- **No blank lines around headings or lists.** Markdown sometimes works without them but renders inconsistently. Always leave blank lines before and after structural elements.
- **Pound signs without spaces.** Write `## Heading`, not `##Heading`. The space matters.
- **Mixing bullet styles.** Pick `-` or `*` and stay consistent within a file.
- **Numbered lists that don't restart.** If you start with `1.` and want a new numbered list later, just start with `1.` again — markdown handles it.
- **Using bold instead of headings.** Headings make the document structure machine-readable. Bold doesn't. If something is a section, use a heading.

---

## Putting it together: a small example

Here's a small skill file in markdown. Read through it and notice the patterns:

````markdown
---
name: meeting-notes-cleaner
description: Takes raw meeting notes and produces a clean summary with decisions, owners, and next steps.
---

# Meeting Notes Cleaner

Use this skill when the user has dropped raw meeting notes into the chat and wants them cleaned up.

## What to produce

A clean meeting summary with these three sections:

1. **Decisions.** Specific choices the group made.
2. **Owners.** Who's doing what next.
3. **Next steps.** When the next meeting is, what needs to happen by then.

## What not to produce

- A literal transcript. The user already has the raw notes.
- A long executive summary. Keep the output short — the meeting summary should be readable in 60 seconds.
- Speculation. If the notes don't say something, don't make it up. Note the gap instead.

## Voice

Match the user's voice profile (see `~/.claude/about-me.md`). Default to direct, prose-driven, short.

## Example output

> **Decisions**
> 1. We're moving the launch from Q2 to Q3.
> 2. Maya owns the new research timeline.
>
> **Owners**
> - Maya: research timeline by Friday.
> - Ravi: revised roadmap by next Wednesday.
>
> **Next steps**
> Next sync: 2026-04-30. Maya brings draft research plan.
````

Notice:

- Front matter with `name` and `description` (this is what triggers the skill)
- H1 for the skill name
- H2 for sections
- A bulleted list for "what not to produce"
- A code block (or could be a blockquote) showing example output
- A reference to another file (`~/.claude/about-me.md`)

You don't need to memorize this structure. You'll see lots of similar files and the pattern will become familiar. Start by writing one yourself for something simple — a meeting notes cleaner, an email draft helper, a one-pager template — and the rest will follow.

---

## Five-minute markdown ramp

If you want to write your first markdown file *right now* to get your hands dirty:

1. Open any text editor.
2. Save a file as `test.md`.
3. Type:

```markdown
# Hello, this is markdown

I'm writing my first markdown file. It has:

- **Bold text** for emphasis
- *Italic text* when I want it
- A list of things, like this one
- A `code-style` word

## A second section

Here's a quoted line:

> Markdown is mostly just text.

That's it. I made a markdown file.
```

4. Save.
5. Paste it into [dillinger.io](https://dillinger.io) or open it in any markdown previewer.
6. Compare the source to the rendered version. Done.

---

## Where to go next

If you want to go deeper, the canonical references are:

- **CommonMark spec** — [commonmark.org](https://commonmark.org) — the official-ish standard markdown
- **GitHub Flavored Markdown** — [github.github.com/gfm](https://github.github.com/gfm) — the slightly extended version most tools use
- **Markdown Guide** — [markdownguide.org](https://markdownguide.org) — a friendly tutorial

For our purposes, you don't need any of these. The cheat sheet above will carry you through every file you write this quarter.
