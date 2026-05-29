# 🤖 Opencode Master Guide — Your Complete Operating Manual

> **Save this in:** `my-dev-journey/_meta/opencode_master_guide.md`
> **Read this file before every session.** It is your cheat sheet for running every session correctly.
> **Do NOT give this file to the AI.** It is FOR YOU — not for Opencode.
> When you're confused about what to do — come here first.

---

## 🧠 The Core Problem (Read This First)

AI has NO memory between sessions. Every time you start Opencode, it starts completely fresh — it doesn't remember you, your project, your rules, or what you did yesterday.

This means YOU are responsible for:
1. **Telling it who you are** — every single session
2. **Telling it where you are** — every single session
3. **Telling it the rules** — every single session
4. **Making it write logs** — so you have a record
5. **Checking it hasn't gone off track** — while you work
6. **Telling it to summarize** — before you stop

**The single most important habit:** Every session, paste the full opening message. Every session. Without exception. Opencode has no memory between sessions — YOU are its memory. The files are its memory. If you don't paste the context, it starts from zero.

---

## 🗂️ Your 6 Files — What Each One Does

Every session, Opencode needs these files **in this order:**

| # | File | What It Does FOR Opencode | When to Give It |
|---|------|--------------------------|-----------------|
| 1 | `context_engineering_master.md` | Tells Opencode WHO you are, your level, your stack, and HOW to behave with you. The most important file. | Every single session — give this FIRST |
| 2 | `historychat.md` | Tells Opencode EVERYTHING that happened in all past sessions | Paste the last 2–3 summary blocks at session start |
| 3 | `chatlog.md` | Opencode reads this to know what happened in THIS session and writes to it during/after | Open alongside your session; tell Opencode to update it |
| 4 | `skill.md` | Tells Opencode EXACTLY what you know and don't know so it doesn't over- or under-explain | Paste the "Skill Snapshot" block at session start |
| 5 | `plan.md` | Tells Opencode WHERE you are in your 6-month journey and WHAT the project is | Paste the relevant phase section at session start |
| 6 | `README.md` | Your folder overview — Opencode doesn't need this, it's for you and GitHub visitors | Only on Day 1, or if Opencode asks about project structure |

---

## 📁 How Your Files Connect to Each Other (The Flow)

```
context_engineering_master.md
        ↓
    (WHO you are + HOW to teach you)
        ↓
    skill.md snapshot
        ↓
    (WHAT you know right now)
        ↓
    historychat.md (last 2–3 summaries)
        ↓
    (WHAT happened before today)
        ↓
    plan.md (current phase section)
        ↓
    (WHERE you are in the 6-month journey)
        ↓
  ┌─────────────────────────┐
  │   OPENCODE SESSION      │
  │   (today's work)        │
  └─────────────────────────┘
        ↓
    chatlog.md
        ↓
    (WHAT happened today — full detail)
        ↓
    historychat.md (new summary added)
        ↓
    skill.md (updated levels)
        ↓
    git push (code saved to GitHub)
```

Everything flows into the next session. Each session feeds the next one.

---

## ✅ PART 1 — Your First-Ever Session (Do This Once Only)

### Step 1 — Set up the folder
```bash
mkdir my-dev-journey
cd my-dev-journey
mkdir projects notes open-source _meta
```
Copy all your `.md` files into the `_meta/` folder.

### Step 2 — Push the folder to GitHub
```bash
git init
git add .
git commit -m "init: start my dev journey"
```
Go to github.com → New Repository → name it `my-dev-journey` → copy the URL, then:
```bash
git remote add origin https://github.com/YOUR-USERNAME/my-dev-journey.git
git branch -M main
git push -u origin main
```

### Step 3 — Open Opencode in your project folder
```bash
cd my-dev-journey
opencode
```
Always run Opencode from INSIDE your project folder. This is how it can see your files.

### Step 4 — Paste the SESSION OPENER (see Part 3 below)

---

## 📅 PART 2 — What to Do Every Day (Full Daily Workflow)

```
BEFORE YOU START (5 minutes)
  ↓
1. Open historychat.md → read your last session summary
2. Open plan.md → check what week you're on and today's task
3. Open chatlog.md → create a new session block at the top
   (copy the template from inside chatlog.md)
4. Open skill.md → find the "Paste Into AI" snapshot block
  ↓
START OPENCODE
  ↓
5. cd my-dev-journey
6. opencode
7. Paste the SESSION OPENER (fill in the blanks — see Part 3)
8. Wait for Opencode to confirm it read all files — don't start coding yet
  ↓
DURING SESSION (2–3 hours)
  ↓
9.  Work step by step — one task at a time
10. Use the CHECK-IN message every 30–45 minutes (see Part 4)
11. git commit after every working feature
12. Add notes to chatlog.md as you go
  ↓
END OF SESSION (15 minutes)
  ↓
13. Paste the SESSION CLOSER (see Part 5) — makes Opencode write the logs
14. Copy SUMMARY BLOCK from chatlog.md → paste into historychat.md
15. Update skill.md if you learned something new
16. git push everything
17. Close Opencode
```

---

## ⚡ PART 3 — The SESSION OPENER (Paste This Every Day, Fill in the Blanks)

```
=== SESSION START ===

STEP 1 — READ THESE FILES FIRST (do not respond until you have read all of them):
- _meta/context_engineering_master.md  ← your rules. Follow ALL of them.
- _meta/historychat.md                 ← read the last 2–3 session blocks
- _meta/chatlog.md                     ← today's session log. You will write to this.
- _meta/skill.md                       ← my exact skill level. Never assume I know more.
- _meta/plan.md                        ← my roadmap. Know what week and phase I'm on.

STEP 2 — CONFIRM you read them by telling me:
- What phase and week am I on right now?
- What did I do in my last session?
- What is my skill level in [the area we're working on today]?
- What is TODAY's goal based on the plan?

STEP 3 — TODAY'S SESSION CONTEXT:
- Date: [FILL IN: e.g. 2025-06-01]
- Phase: Month [X], Week [X]
- Project: [FILL IN: e.g. "Phase 0 Setup" or "Project 1 — Landing Page"]
- Where I left off: [FILL IN: copy 2–3 lines from historychat.md OR write "First session ever"]
- Today's goal: [FILL IN: one specific thing — e.g. "Set up my folder structure and push to GitHub"]
- I am stuck on / confused about: [FILL IN: or write "Nothing yet"]
- My current code: [FILL IN: paste relevant code OR write "Starting fresh"]

STEP 4 — RULES REMINDER (always follow these):
- Explain EVERY line of code. What it does. Why it's there. What breaks if I remove it.
- One step at a time. Wait for me to say "done" before moving to the next step.
- After every working feature, remind me to: git add . && git commit -m "message" && git push
- Never give me a wall of code. Break it into the smallest possible pieces.
- If I am confused, slow down and use a simpler analogy.
- At the END of this session, update _meta/chatlog.md with the full session summary.

Now confirm you read everything and tell me the 4 things from STEP 2.
=== END ===
```

**If Opencode confirms correctly → you're ready to work.**
**If it gets something wrong → paste the SESSION OPENER again and say "Re-read the files."**

---

## 🔄 PART 4 — Exact Prompts to Use While Working

### 🟢 To start a task

```
I want to [describe what you want to build in plain English].
Start by explaining what we need to do BEFORE writing any code.
Then build it step by step — one piece at a time.
Wait for me to say "done" or "I understand" before moving on.
```

---

### 🔵 When Opencode writes code — say this every time

```
Before you write any code, explain to me:
1. What this code does in plain English
2. Why we need it here
3. What would break if we removed it
4. Is there another way to do this? What are the trade-offs?

Then write the code in small chunks — one step at a time.
Wait for me to say "I understand" or "done" before moving to the next step.
```

---

### 🟡 When you don't understand something

```
Stop. I don't understand [the specific thing].
Explain it to me like I have never heard of it before.
Use a real-world analogy first, then show me the code.
Don't move forward until I confirm I understand.
```

---

### 🔵 To verify you understood

```
I'm going to explain this back to you in my own words.
Tell me if I understood it correctly or where I went wrong:
[write your explanation here]
```

**Why this works:** This is how you know if you truly understood — not just nodded along. If you can explain it back, you own it. If you can't, you caught the gap before it causes problems later.

---

### 🟣 To check if you ACTUALLY understood (not just think you did)

```
I am going to explain what we just did back to you in my own words.
Tell me if I understood it correctly, or where I went wrong:
[write your explanation here in simple words]
```

Use this after any concept that felt complex or fast. It is not the same as the blue prompt above — this one is specifically for moments when you're not sure if you really got it or just followed along.

---

### 🟠 CHECK-IN — Paste this every 30–45 minutes

```
=== CHECK-IN ===
Stop and tell me:
1. What have we done so far in this session?
2. What step are we on right now and what is the current state of the code?
3. What is the next step after this?
4. Are we still on track with today's goal: [repeat your goal here]?
5. Is there anything I should understand before we continue?
=== END ===
```

**Why this works:** This forces Opencode to "reset" its understanding and catch any drift before it gets worse. It also helps YOU stay aware of where you are.

---

### 🔴 When Opencode seems off track or confused

```
Stop. I think we've drifted from the goal.
Our goal for today was: [restate your goal]
What we have actually done so far: [describe]
Re-read _meta/plan.md and _meta/context_engineering_master.md.
Are we still working toward that goal?
If not, what went wrong and how do we get back on track?
```

---

### 🐛 When You Hit an Error — Say this (do NOT skip this prompt)

```
I got this error: [paste the EXACT full error message]

Before you fix it, explain:
1. What does this error mean in plain English?
2. What caused it?
3. Where exactly in the code is the problem?
4. How should we think about fixing it?

Then fix it step by step. Explain each change.
```

**Why this matters:** Never let Opencode silently fix an error. If you don't understand what broke and why, you will hit the same error again — and next time you won't know how to handle it.

---

### 🔍 To verify Opencode is not hallucinating — say this when something feels wrong

```
I want to verify this before we continue.
Show me exactly where in the code this is happening.
Don't explain — show me the actual file and line number.
```

and/or:

```
Are you certain about this? If you're not 100% sure, say so.
I would rather you say "I don't know" than give me a wrong answer.
```

**Why this works:** Opencode (like all AI) sometimes confidently states wrong things. Asking it to show you the actual code or admit uncertainty catches most hallucinations before they cause problems.

---

### ⬜ When you want an alternative approach

```
Is there another way to do what we just built?
Show me one alternative and explain the difference in simple terms.
Which one would a real company use and why?
```

---

### 🌿 To start a new feature or new file

```
Before we write anything:
1. What folder should this file go in and why?
2. What should we name it and why?
3. How does this connect to what we already built?
4. What is the simplest possible version we can build first?
```

---

### 🧠 To make Opencode update your skill file

```
Based on what we worked on today, tell me:
- Which skills in my skill.md should I update?
- What level should each one move to (⬜ → 🟡 → 🟠 → 🟢 → ✅)?
- Which new skills should I add that aren't in the file yet?
```

---

### 🔀 For open source work (GitHub contributions)

```
I want to contribute to this open source project: [paste repo URL]

Help me:
1. Understand what this project does before touching any code
2. Find a good first issue suitable for my skill level
3. Understand what the issue is asking me to do
4. Walk me through the fork → clone → branch → code → PR workflow
5. Review my code before I submit the PR

Go slowly. I am new to contributing to other people's code.
```

---

## 🔒 PART 5 — How to Prevent Hallucination and Keep Opencode on Track

**Hallucination** = AI confidently tells you something wrong, or invents code that doesn't work. This happens when AI "guesses" instead of using your actual files.

### Rule 1 — The Confirm Rule: Always make it CONFIRM before starting

Never let Opencode just start working. The SESSION OPENER handles this — always wait for the confirmation before coding.

```
Before you write any code — tell me:
1. What phase and week am I on?
2. What is my skill level in this area?
3. What exactly are we building today?
If any of these are wrong, stop and I'll correct you.
```

### Rule 2 — The Reset Rule: Use the CHECK-IN every 30–45 minutes (see Part 4)

This forces the AI to reset and confirm it hasn't drifted. Do it even when things seem fine.

### Rule 3 — The Brake Rule: If it writes code you don't understand, STOP IT

```
Wait. Before we continue — I don't understand what we just wrote.
Do not add anything new yet.
Go back and explain [specific part] in the simplest way possible.
```

### Rule 4 — The Chunk Rule: Never let it write more than 20–30 lines without explaining

```
Stop before writing more code.
Explain what you're about to write and WHY before you write it.
I want to understand the plan before I see the code.
```

### Rule 5 — The Contradiction Rule: If it contradicts itself, call it out

```
Earlier you said [X] but now you're saying [Y].
Which is correct and why? Show me the evidence in the actual code.
```

### Warning Signs — Know the signals

| Sign | What It Means | What to Say |
|------|--------------|-------------|
| Writes code you don't understand at all | Going too fast | "Stop. Explain the last thing you wrote before continuing." |
| Skips explaining a line | Breaking the rules | "You didn't explain that line. What does it do and why?" |
| Writes 50+ lines at once | Going too fast | "Too much at once. Break this into smaller steps." |
| Uses a word you don't know | Assumed knowledge | "What is [word]? Explain it in one sentence before continuing." |
| Contradicts what it said earlier | Hallucinating | "Earlier you said [X] but now you're saying [Y]. Which is correct and why?" |
| Seems to be building the wrong thing | Off track | "Stop. Re-read my goal for today. Is this still heading toward that?" |
| Says 'just do X' without explaining | Breaking the rules | "Don't say 'just'. Explain what X is and why I need to do it." |

### Rule 6 — Root causes of drift and how to stop them

| Problem | What Causes It | How to Prevent It |
|---------|---------------|-------------------|
| Forgets your level | Long session, no reminder | Paste skill snapshot at start every time |
| Goes off-topic | Vague goals | Give ONE specific goal per session, not many |
| Confidently wrong | No verification | Use the CHECK-IN prompt every 30–45 min |
| Loses session context | Long conversations | Paste the full SESSION OPENER every single time |
| Skips explaining code | No reminder | Add "explain every line" to every code request |

---

## 📝 PART 6 — The SESSION CLOSER (Paste This at the End of Every Session)

```
=== SESSION CLOSER ===

We are done for today. Before I close, do these 4 things IN ORDER:

THING 1 — Update _meta/chatlog.md
Fill in ALL the sections in today's session block:
- What I Actually Did (bullet points of everything we built)
- What I Learned (explain each concept in simple words a beginner would use)
- What Confused Me (be honest — what was hard today)
- Blockers (any errors we hit and how we fixed them)
- Files Changed (list every file we created or edited and why)
- Git commits made
- Goal for Next Session (what should I start with next time?)

THING 2 — Write the SUMMARY BLOCK
Write the full summary block at the bottom of today's chatlog entry.
Use this exact format:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DATE: [today's date]
PROJECT: [project name + phase]
WHAT WAS DONE:
  - [bullet 1]
  - [bullet 2]
  - [bullet 3]
WHAT WAS LEARNED:
  - [short explanation in simple words]
BLOCKER (if unresolved):
  - [describe any unresolved issue, or write "None"]
NEXT SESSION GOAL:
  - [exactly what to start next time]
GIT STATUS: Pushed ✅ / Not pushed ❌
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

THING 3 — Update _meta/skill.md
List every skill we practiced today.
Tell me which icon to change each one to: ⬜ → 🟡 → 🟠 → 🟢 → ✅

THING 4 — Give me my git commit message
Write a good commit message for today's work in this format:
feat: [describe what was built]
Example: feat: set up folder structure and pushed to GitHub

Then remind me to run:
git add .
git commit -m "[the message you just wrote]"
git push
=== END ===
```

After Opencode does all 4 things:
- Copy the SUMMARY BLOCK it wrote → paste it at the top of `historychat.md`
- Run the git commands it gave you

---

## 📊 PART 7 — Your File System at a Glance

```
my-dev-journey/
├── _meta/
│   ├── context_engineering_master.md  ← GIVE THIS EVERY SESSION. Rules + who you are.
│   ├── plan.md                        ← GIVE THIS EVERY SESSION. Your roadmap.
│   ├── skill.md                       ← GIVE THIS EVERY SESSION. Your skill level.
│   ├── chatlog.md                     ← GIVE THIS EVERY SESSION. Opencode writes here.
│   ├── historychat.md                 ← GIVE THIS EVERY SESSION. Opencode reads last 2–3 entries.
│   ├── README.md                      ← Give only on Day 1 or when starting a new project.
│   └── opencode_master_guide.md       ← This file. Read it before every session. Don't give to AI.
├── projects/
├── notes/
└── open-source/
```

---

## ⚠️ PART 8 — Common Mistakes and How to Avoid Them

| Mistake | What Happens | What to Do Instead |
|---------|-------------|-------------------|
| Starting a session without pasting context | Opencode treats you as a stranger and skips explanations | Always paste the full SESSION OPENER first |
| Accepting code you don't understand | You get stuck in the next session | Stop and ask "explain every line" before moving on |
| Setting too many goals in one session | Nothing gets finished properly | Pick ONE goal per session and finish it completely |
| Skipping chatlog.md at session end | You lose the context for next session | 5 minutes at end = saves 30 minutes next session |
| Not pushing to GitHub | Work gets lost, no progress history | `git push` is the last thing you do every session |
| Moving on when confused | Confusion stacks up and becomes overwhelming | Say "Stop. I don't understand X." every single time |

---

## 🗓️ PART 9 — Your Week at a Glance

| Day | What to Do |
|-----|-----------|
| Mon | Learn a new concept — ask Opencode to explain it, build a tiny example |
| Tue | Apply it — build the next feature of your current project |
| Wed | Continue building — one step further |
| Thu | Continue building + update skill.md at the end |
| Fri | Open source work: find an issue, make a contribution, or do a code review |
| Sat | Review the week: clean up messy code, read what you wrote |
| Sun | Update historychat.md weekly review, plan next week's goal |

---

## 🔁 PART 10 — Quick Reference Card (Print This or Keep It Open)

```
EVERY SESSION:
  cd my-dev-journey
  opencode
  → paste SESSION OPENER (fill in date, phase, project, goal)
  → wait for Opencode to confirm it read everything before coding

EVERY 30–45 MINUTES:
  → paste the CHECK-IN message

WHEN WRITING CODE:
  → "Before you write any code, explain what it does and why."

WHEN STUCK OR CONFUSED:
  → "Stop. Explain [specific thing] before we continue."

WHEN SOMETHING BREAKS:
  → "Explain the error first. Then fix it step by step."

AFTER EVERY WORKING FEATURE:
  → git add . && git commit -m "feat: describe what you built" && git push

END OF SESSION:
  → paste SESSION CLOSER
  → copy SUMMARY BLOCK → paste into historychat.md
  → update skill.md
  → run git push
  → close Opencode
```

---

## ❗ The Most Important Rule

**The AI is a tool. YOU are in control.**

If the AI goes too fast → stop it.
If the AI writes something you don't understand → stop it.
If the AI seems off track → stop it.

You are never "bothering" the AI by asking it to slow down, repeat, or re-explain.
That is exactly what it's there for.

---

*Read before every session | Do not give this file to Opencode | Last updated: [DATE]*
