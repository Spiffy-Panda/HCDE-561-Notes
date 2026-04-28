---
title: "Personal Context File — Student Guide"
---

HCDE 561: Strategic Human-Centered AI

**Exercise: Your Personal Context File**

Duration: 60 minutes. Format: Pair interview, then partner test, then solo polish at home. Output: A markdown file you can drop into any AI tool, every time, that dramatically improves the quality and fit of what you get back.

## Why We’re Doing This

Without context, an AI model treats you as a generic professional with no specific role, no voice, no standards, no real work. The output is generic back: vague, middle-of-the-road, stripped of the particulars that would make it useful. You’ve probably felt this.

The fix is simple and underrated: **give the model a file about you that it can read every time.** A good personal context file answers, in the model’s first few seconds of reading, the questions a new colleague would spend weeks figuring out: who are you, what do you do, how do you think, how do you communicate, what do you care about, what would you never say, who are you usually working for or with.

Every AI tool you’ll use this quarter — ChatGPT, Claude, UW Purple, Claude Code, Cursor, whatever — can take this file. Custom GPTs and Claude Projects load it as knowledge. Claude Code references it from your project’s CLAUDE.md. Chat tools accept it as a pasted or uploaded reference. It is the most portable, highest-leverage artifact you can build for your own AI practice. Build it once, reuse it everywhere.

**A note on naming and architecture.** Save this file as about-me.md (or about-me-context.md — your choice, consistent). Keep it separate from any project CLAUDE.md file. The CLAUDE.md file belongs to the *project* — its conventions, structure, and workflow. The about-me.md file belongs to *you* — and you reference it from CLAUDE.md. This separation means one source of truth for who you are, portable across every project you touch.

The tricky part is that it’s very hard to write yourself into a file from a blank page. Voice goes flat. You under-share the specific things. You skip what feels obvious to you, which is exactly the stuff the model doesn’t know. So instead of drafting solo, you’re going to interview each other.

## The Exercise

### Step 1 — Pair up (2 min)

Find a partner. **Pick someone who is not in your field.** This matters. If your partner already knows your domain, they’ll fill in blanks with their own assumptions and ask shallower questions. A stranger to your work will ask the questions you actually need to answer.

Introduce yourselves with just your name and what you do in one sentence. Don’t go deeper yet — save it for the interview.

### Step 2 — Interview each other (30 min, ~15 min each direction)

Decide who goes first. You’ll swap halfway.

**When you’re the interviewee:**

- Talk. The interviewer is going to ask questions from a prompt sheet. Answer them in plain speech. Don’t edit yourself. Don’t tidy up what you say for how it’ll read.
- If a question doesn’t apply to you, say so and move on.
- If a question pulls something unexpected out of you, follow it. The best parts of your context file are the things you didn’t expect to say.
**When you’re the interviewer:**

- Use the interview prompt sheet. Ask the questions. Ask follow-ups when something’s interesting.
- **Your job is to write the draft of their context file as they talk.** Not a transcript. A draft. You’re catching the shape of them.
- Write in their voice, as best you can. If they say “I hate bullet points,” write that down as “I hate bullet points” — not “The subject prefers prose to bulleted formats.”
- At the end, read them back what you wrote. They’ll correct things. Capture the corrections.
Keep moving. Don’t perfect any one section. First drafts are the goal, not finished artifacts.

### Step 3 — Partner test (10 min)

You each now have a first draft of your own context file, written by someone who listened to you.

Swap back. The partner who drafted your file is going to try to answer a question **as you**, using only the file. Questions like:

- How would you respond to an urgent email from your least favorite stakeholder?
- What are the three things you’d want known before a new team member started working with you?
- What’s a task you’d hand off to an AI tomorrow? One you’d never hand off?
Listen to your partner’s answer. Does it sound like you? Where does it drift? What did they miss?

The drift *is the data*. Everything your partner got wrong — or couldn’t answer — is a gap in the file that needs to be filled. Mark those gaps.

### Step 4 — Take it home (homework, ~30-45 min)

Finish the file this week. Use the example context file as a reference for what a complete one looks like.

You’ll bring it to Week 6. From Week 6 onward, it’s the file you load into whatever tool you’re using, every time. It’s a living document — update it as you learn what your AI tools actually need from you.

## What a Good Context File Looks Like

Review the example file to see the level of specificity that makes a difference. Some patterns that matter:

- **Specific, not abstract.** “I manage a team of six designers working on enterprise SaaS” beats “I work in product design.” Names of tools, names of standards, names of the stakeholders you deal with.
- **Voice samples.** Include 2-3 sentences in your actual writing voice so the model can match it.
- **Anti-patterns included.** “Never use em dashes. Never use the word ‘leverage.’ Never write introductions that announce what the email is about before saying anything.” These save you more re-writes than positive instructions.
- **Constraints and standards.** The things you’d never ship. The quality bar. The process you follow.
- **Common collaborators.** The specific people or roles you write for, argue with, report to. Model needs to know the audience.
- **Explicit non-expertise.** What you’re *not* an expert in matters. Keeps the model from playing up to you in your weak areas.
Aim for 400-800 words. Shorter than you think. Dense with specifics. A context file that’s 2,000 words is probably a context file that’s wasting tokens on things the model will ignore.

## Other Approaches (If You Want to Try a Different Method at Home)

The pair interview is the default because social reflection pulls out specifics a blank page won’t. But the *goal is the artifact, not the method*. If you want to revise, extend, or re-do your file at home using a different approach, these all work — and a few will produce a different kind of artifact that’s worth generating alongside the pair-interview draft.

**1. AI-conducted interview.**

Upload the AI interviewer file (ai-interviewer.md) to Claude Chat (or ChatGPT, or any capable AI chat tool). Say: *“I’d like to run this. Please begin the interview.”* The AI will run the interview using the same protocol your partner used, then synthesize a context file for you. Often the follow-ups are sharper than a human partner’s because the model has no social friction about pushing. Good for introverts, good for finishing or refining at home, and it’s a real demonstration of using AI to improve your AI practice.

**2. Solo guided drafting.**

Use the interview prompt sheet by yourself. Answer each question in writing. Slower and flatter than the pair or AI-interview versions, but a reasonable fallback if you missed class.

**3. Transcript + synthesis.**

Record yourself talking through your work for 10-15 minutes — answering prompts or just freestyling about a recent project. Run the transcript through an AI to extract voice samples, common phrases, and themes. Edit into a context file. Good for people whose speaking voice differs significantly from their writing voice. Decide which one you want the file to capture.

**4. Archaeology from existing work.**

Pull 5-10 pieces of your own writing — recent emails, a memo you’re proud of, a proposal, a slack message. Read them critically. Notice patterns: how you open, how you close, words you use, structures you favor. Write the context file from what you find. Good if you hate introspection but have a lot of output. Produces a descriptive file (what you actually do) rather than a prescriptive one (what you aspire to).

**5. Iterative drafting with AI feedback.**

Draft a rough version solo (10 min). Paste into Claude or ChatGPT with: *“Here’s my draft context file. Interview me about what’s missing, generic, or unclear. Help me tighten it.”* Iterate through a few rounds. Good for students who like to start by writing and refine through conversation.

Most students will do the pair interview in class, then polish solo or iterate with the AI interviewer at home. The AI-interviewer pathway (method 1) is strongly recommended as a second pass — it often surfaces things the pair interview missed.

## What to Bring to Week 6

- A completed personal context file, saved as about-me.md or about-me-context.md (your choice — you’ll use this name everywhere this quarter)
- Your shortlist of 4-5 candidate use cases (from the brainstorm exercise)
Come ready to load your context file into the tool you’ve chosen and start building your first use case.
