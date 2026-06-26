# Threads Post Scorer

AI-powered scoring tool for Threads posts. Get a 0-100 score, line-by-line diagnosis, and an improved rewrite — all calibrated to your personal brand.

## What It Does

Paste your draft → get three things back:

1. **Score (0-100)** across 8 dimensions: Hook Power, Conversation Pull, Emotional Resonance, Originality, Format & Rhythm, Action Trigger, Brand Fit, and Reach-Killer Detection
2. **Line-by-line diagnosis** — every sentence marked 🟢 (strong), 🟡 (improvable), or 🔴 (reach-killer) with specific reasons
3. **Rewrite** targeting 70+ score, preserving your ideas in a more effective format

## Personal Calibration

The first time you use it, the scorer asks 3-5 quick questions:

- What platform? (Threads / IG / X / LinkedIn)
- What are your content topics?
- What's your posting goal? (grow followers / sell / build authority / share)
- Who is your audience? *(optional)*
- Paste your best post *(optional — this reverse-engineers your voice)*

Your answers are saved to `MY_PROFILE.md`. Every score after that is calibrated to you. Say "recalibrate" anytime to redo it.

## How to Install

### Claude Code (CLI / Desktop / Web)

Copy `SKILL.md` to your Claude Code skills directory:

```bash
# Create skill directory
mkdir -p ~/.claude/skills/threads-post-scorer

# Copy the skill file
cp SKILL.md ~/.claude/skills/threads-post-scorer/SKILL.md
```

Then start Claude Code and say "score this post" or paste a draft.

### Other AI Tools

Copy the contents of `SKILL.md` into your system prompt or custom instructions. The scoring rubric works with any LLM that follows structured instructions.

## Score Ranges

| Range | Meaning |
|-------|---------|
| 80-100 | Post it. High chance of strong performance |
| 70-79 | Minor tweaks. Adjust hook or call-to-action |
| 50-69 | Structural issues. Needs rewriting |
| 0-49 | Consider a different angle |

## Example

**Input:**
> I've been using AI tools for 6 months and here are my top 5 takeaways for beginners.

**Output:**
```
Score: 42/100

Hook Power: 5/15 — Generic "here are my takeaways" opening. No conflict or surprise.
Conversation Pull: 3/20 — No question, no debate trigger. Readers have nothing to respond to.
...

Rewrite (Target: 70+):

"6 months ago I couldn't even spell ChatGPT. Yesterday my AI system wrote 3 articles while I slept.

Here's what I wish someone told me on day 1..."
```

## Research Basis

Scoring is based on:
- Meta's official content distribution guidelines
- Buffer's analysis of 2.5M Threads posts (best posting times) and 45M posts (best formats)
- Platform-specific algorithm documentation

See the full source list at the bottom of `SKILL.md`.

## License

MIT — use it however you want.

---

Built by [Allen](https://www.threads.net/@allenchiu0903) — a 52-year-old solo entrepreneur who uses AI to build systems that work while he sleeps. Follow for more AI workflow tools and real-world automation stories.
