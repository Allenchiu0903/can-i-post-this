# Can I Post This?

[繁體中文版 README](README-zh-TW.md)

AI-powered post scorer for Threads, Instagram, X, and LinkedIn. Paste a draft, get a 0-100 score + line-by-line diagnosis + rewrite — calibrated to your personal brand.

## What It Does

Paste your draft → get three things back:

1. **Score (0-100)** across 8 dimensions: Hook Power, Conversation Pull, Emotional Resonance, Originality, Format & Rhythm, Action Trigger, Brand Fit, and Reach-Killer Detection
2. **Line-by-line diagnosis** — every sentence marked 🟢 (strong), 🟡 (improvable), or 🔴 (reach-killer) with specific reasons
3. **Rewrite** targeting 70+ score, preserving your ideas in a more effective format

## Personal Calibration

The first time you use it, the scorer asks 3-5 quick questions:

- What platform do you post on? (Threads / IG / X / LinkedIn)
- What are your content topics? List 3-5 keywords
- What's your posting goal? (grow followers / sell / build authority / share)
- Who is your audience? *(optional)*
- Paste your best post *(optional — reverse-engineers your writing voice)*

Your answers are saved to `MY_PROFILE.md`. Every score after that is calibrated to you, not a one-size-fits-all template. Say "recalibrate" anytime to redo it.

## How to Install

### Claude Code (CLI / Desktop / Web)

Copy the skill file to your Claude Code skills directory. Choose English or Traditional Chinese:

```bash
# Create skill directory
mkdir -p ~/.claude/skills/can-i-post-this

# English version
cp SKILL.md ~/.claude/skills/can-i-post-this/SKILL.md

# Traditional Chinese version (繁體中文)
cp SKILL-zh-TW.md ~/.claude/skills/can-i-post-this/SKILL.md
```

Start Claude Code and say "score this post" or paste a draft.

### Other AI Tools (ChatGPT / Gemini / any LLM)

Copy the contents of `SKILL.md` (or `SKILL-zh-TW.md`) into your system prompt or custom instructions. The scoring rubric works with any LLM that follows structured instructions.

## Score Ranges

| Range | Meaning |
|-------|---------|
| 80-100 | Post it. High chance of strong performance |
| 70-79 | Minor tweaks. Adjust hook or call-to-action |
| 50-69 | Structural issues. Needs rewriting |
| 0-49 | Consider a different angle |

## Example

**Input:**
> Just turned 52 and started learning AI from zero. No coding background, couldn't even use ChatGPT six months ago.
>
> Now my AI system automatically crawls 40+ news sources at 4am, generates 3 social media drafts, and creates image assets. I wake up and just pick one to post.

**Output:**
```
Score: 82/100

Hook Power: 14/15 — Age contrast + question format, immediately triggers curiosity
Conversation Pull: 12/20 — Strong ending but closed. No open question inviting replies
Emotional Resonance: 14/15 — Triple denial stacking pain points, 4am scene recreation
Originality: 9/10 — First-person real experience + specific numbers
...

Rewrite (Target: 85+):

Just turned 52 and started learning AI. No coding, no tech background.

Six months ago I was copy-pasting ChatGPT prompts like everyone else.

Today my system runs at 4am while I sleep — 40+ sources crawled,
3 drafts written, images generated.

I wake up and pick one to post. That's it.

The real question isn't whether you're too old.
It's whether you're willing to spend time figuring out one new thing.

What's the step you're stuck on right now? Tell me — I'll break it down.
```

## Research Basis

Scoring is based on:
- Elon Musk's verified public statements on X algorithm goals ([original posts](https://x.com/elonmusk/status/1875355425601999255))
- X algorithm open-source code (dwell time weights, native content boost, originality signals)
- Meta's official content distribution guidelines (Engagement Bait policy)
- Buffer's analysis of 2.5M Threads posts (best posting times) and 45M posts (best formats)

Full source list with links at the bottom of `SKILL.md`.

## License

MIT — use it however you want.

---

Built by [Allen](https://www.threads.net/@allenchiu0903) — a 52-year-old solo entrepreneur using AI to build systems that work while he sleeps. Follow for more AI workflow tools and real-world automation stories.
