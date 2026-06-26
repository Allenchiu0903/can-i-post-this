# 這篇能發嗎 — Can I Post This?

> 貼上草稿，拿到 0-100 分 + 逐句診斷 + 改寫版。
> Paste a draft, get a score 0-100 + line-by-line diagnosis + rewrite.

## Trigger

Activate when the user says any of these:
- "score" "rate this" "can this go viral?" "check this post"
- "threads score" "rate my post" "is this good enough?"
- Or pastes text expecting Threads posting advice

## First-Time Setup: Personal Calibration

If no `MY_PROFILE.md` file exists in the skill directory, run calibration before scoring. Ask these questions one at a time:

### Question 1 (Required)
"What platform do you mainly post on?"
- Threads / Instagram / X (Twitter) / LinkedIn / Other

→ This determines format rules and reach-killer detection. Each platform has different algorithms and penalizes different things.

### Question 2 (Required)
"What are your 3-5 content topics? (e.g. AI, fitness, parenting, investing)"

→ This replaces the default topic list and becomes your brand consistency benchmark. Posts outside your topics score lower on brand fit.

### Question 3 (Required)
"What's your main goal for posting?"
- Grow followers
- Sell a product or service
- Build professional authority
- Share for fun / document my journey

→ This shifts scoring weights:
- Grow followers → Hook Power and Conversation Pull weighted higher
- Sell → Action Trigger weighted higher
- Authority → Originality weighted higher
- Share/document → Emotional Resonance weighted higher

### Question 4 (Optional)
"Who is your audience? Describe in one sentence."
(e.g. "30-something parents learning to code" or "small business owners in Taiwan")

→ Adjusts tone and emotional resonance benchmarks.

### Question 5 (Optional)
"Paste your best-performing post — the one you're most proud of."

→ The scorer analyzes it to reverse-engineer your voice: sentence length, tone, structure patterns. This is more accurate than any questionnaire.

### After Calibration

Save results as `MY_PROFILE.md` in the skill directory:

```markdown
# My Scoring Profile

- Platform: [answer]
- Topics: [answer]
- Goal: [answer]
- Audience: [answer or "not specified"]
- Voice sample: [answer or "not provided"]
- Calibrated: [date]

## Derived Settings
- Brand topics: [list from Q2]
- Weight adjustments: [derived from Q3]
- Tone benchmark: [derived from Q5 or default]
- Platform-specific rules: [derived from Q1]
```

Tell the user: "Profile saved. You can update it anytime by saying 'recalibrate'. Now paste your first draft."

On subsequent uses, read `MY_PROFILE.md` silently and score immediately.

## Scoring Flow

After receiving a draft, execute three steps in order:

### Step 1: Score (0-100)

Score across 8 dimensions, each scored independently then summed:

| Dimension | Points | Criteria |
|-----------|--------|----------|
| **Hook Power** | 0-15 | Do the first two sentences stop the scroll? Controversial claim (15) > Counter-intuitive (12) > Series format "X happened again" (12) > Question (10) > Number-led (8) > No hook (0-3) |
| **Conversation Pull** | 0-20 | Does the reader want to reply? Open question ending (18-20) > Controversial stance sparking debate (15-18) > Self-assessment framework "which level are you?" (12-15) > Info dump with no conversation space (0-5) |
| **Emotional Resonance** | 0-15 | Does it trigger a real feeling? Pain-point stacking + scene recreation (15) > Real mistake/lesson (13-14) > Relatable insight (10-12) > Interesting but shallow (6-9) > Cold information (0-5) |
| **Originality** | 0-10 | Does it contain the author's unique perspective/experience/data? First-hand experience (8-10) > Personal opinion + example (5-7) > Curated public info (2-4) > Pure repost (0-1) |
| **Format & Rhythm** | 0-10 | Line breaks, sentence length, reading flow. Short sentences mixed + proper breaks (8-10) > Clear paragraphs (5-7) > Wall of text (0-3) |
| **Action Trigger** | 0-10 | Does the reader have a reason to save/share? Actionable steps worth saving (8-10) > Quotable line worth sharing (5-7) > Read and leave (0-3) |
| **Brand Fit** | 0-10 | Is it within the user's defined topics + matching their tone? Perfect match (8-10) > Related but drifting (4-7) > Off-topic (0) |
| **Reach-Killer Detection** | 0-10 | Deduction-based. No reach killers (10) > Minor issues (7) > Obvious problems (0-5) |

**Reach-Killer Checklist** (each hit deducts 2-3 points):
- Engagement bait: "comment YES" "reply 1 for link" "agree?"
- Sales pressure: "limited time" "discount" "click link" "referral code"
- Recycled content feel: looks copy-pasted from IG/FB
- Wall of text: more than 5 lines without a break
- Corporate/PR tone
- Information only, no perspective (reads like Wikipedia)
- External links (Threads algorithm suppresses posts with links)

**Platform-Specific Reach Killers:**
- Threads: external links, hashtag spam (>5), @mention spam
- Instagram: link in caption (no clickable links anyway), engagement bait
- X/Twitter: thread-jacking feel, too many hashtags
- LinkedIn: emojis overload, "I'm humbled" clichés

**Advanced Hook Patterns:**

Series Format: Use "X happened again" or "Today X went crazy again" to build a recurring column hook. Readers see it and know "there's something good again," building a follow habit.

Pain-Point Stacking: Don't just name one pain point — list 3-7 specific scenarios so the reader thinks "this person totally gets me." Stack the list, then follow with scene recreation for maximum emotional resonance.

**Score Ranges:**
- 80-100: Post it. High chance of strong performance
- 70-79: Minor tweaks needed. Adjust hook or CTA
- 50-69: Structural issues. Needs rewriting
- 0-49: Consider starting over. Core direction may need rethinking

### Step 2: Line-by-Line Diagnosis

Mark every sentence in the draft:

- 🟢 **Strong**: Has hook power / triggers reply / emotional resonance / quotable
- 🟡 **Improvable**: Right direction but weak expression / could be more conversational / rhythm off
- 🔴 **Reach-Killer**: Will suppress reach / too formal / engagement bait / no conversation space

Each mark includes a one-line explanation.

Example:
```
🟢 "Two months ago I completely integrated Claude into my workflow and noticed something."
   → Strong hook: first-person + time frame + suspense (noticed what?)

🟡 "If you're still manually writing scripts and moving data around, you're doing manual labor in the AI age."
   → Good point but too long. Split into two sentences for better rhythm.

🔴 "Follow me for more AI tool tips!"
   → Reach-killer: PR tone + no conversation space. Change to a question: "What's the most painful manual process in your workflow right now?"
```

### Step 3: Rewrite

Based on the diagnosis, produce a rewrite targeting 70+ score. Rules:

1. **Hook rewrite**: If original hook < 10, rewrite the first two sentences
2. **Ending rewrite**: If no conversation trigger, add an open question or self-assessment framework
3. **Format restructure**: Short sentences first, proper line breaks, key sentences on their own line
4. **Conversational tone**: Replace formal language with natural speech
5. **Preserve intent**: Change the expression, not the ideas

The rewrite also includes:
- Suggested format: text only / text+image / self-reply thread
- If thread is recommended: suggested split (how many replies, focus of each)

## Self-Reply Thread Recommendations

Suggest a self-reply thread when any of these apply:
- Content exceeds 300 characters (beyond optimal single-post length)
- Contains 3+ steps or points
- Can use a "Part 1/N" structure
- Topic suits progressive disclosure (opinion → example → how-to → CTA)

Three thread templates:

**Template A — Progressive** (opinion posts):
```
Main post: Controversial hook + core claim
 ↳ Reply 1: Why (reasoning/data)
   ↳ Reply 2: How (specific steps)
     ↳ Reply 3: CTA question (invite discussion)
```

**Template B — Serial** (tutorial posts):
```
Main post: Hook + Part 1/5
 ↳ Reply: Part 2/5
   ↳ Reply: Part 3/5
     ↳ Reply: Part 4/5
       ↳ Reply: Part 5/5 + CTA
```

**Template C — Suspense** (engagement posts):
```
Main post: Strong hook + "Details in the replies 👇"
 ↳ Replies 1-N: Actual content
 ↳ Final reply: CTA + follow invite
```

## Algorithm Reference (Scoring Basis)

Scoring references these known algorithm factors:

| Factor | Weight | Notes |
|--------|--------|-------|
| Engagement Velocity | Highest | Interactions in the first 30-60 minutes determine distribution |
| Reply Depth | Very High | Reply-to-reply = significantly more weight than top-level likes |
| Save + Share | High | Signals high value, worth more than likes |
| Dwell Time | Medium-High | Longer reading time = more distribution |
| Originality | Medium-High | Recycled content gets suppressed |
| Image+Text | Medium | Image posts get higher engagement than text-only |
| Content Freshness | Medium | New posts get a boost |
| Positive/Constructive | Medium | Negative/attacking content gets suppressed |

## Posting Time Suggestions

| Time Slot | Recommendation |
|-----------|---------------|
| Weekday 7-10am | Best (global data + morning commute) |
| Weekday 12-1pm | Good (lunch break scrolling) |
| Weekday 9-10pm | Worth testing (evening wind-down) |
| Saturday all day | Avoid (lowest engagement globally) |
| Sunday 10-11am | OK (lazy morning scrolling) |

Note: Adjust for your timezone and audience. These are based on global data from 2.5M posts.

## Output Format

Fixed output structure for every scoring:

```
## Score: XX/100

| Dimension | Score | Note |
|-----------|-------|------|
| Hook Power | X/15 | ... |
| Conversation Pull | X/20 | ... |
| Emotional Resonance | X/15 | ... |
| Originality | X/10 | ... |
| Format & Rhythm | X/10 | ... |
| Action Trigger | X/10 | ... |
| Brand Fit | X/10 | ... |
| Reach-Killer Detection | X/10 | ... |

## Line-by-Line Diagnosis

[Each sentence marked 🟢🟡🔴 + reason]

## Rewrite (Target: 70+)

[Rewritten post]

Suggested format: text only / text+image / self-reply thread (N replies)
Suggested posting time: [based on user's timezone]
```

## Honesty Boundaries

- The score is a **prediction** based on public algorithm factors, not a guarantee
- Threads' algorithm changes constantly; weights may shift
- Regional culture affects performance — global strategies don't always apply locally
- Some engagement multipliers cited in research are approximations
- This skill cannot replace the feedback loop of actually posting and observing real data
- When in doubt, post it. Real data beats predictions every time

## Research Sources

### Primary Sources
- [Meta Transparency Center — Engagement Bait](https://transparency.meta.com/features/approach-to-ranking/content-distribution-guidelines/engagement-bait)
- [Buffer — Best Time to Post on Threads (2.5M posts)](https://buffer.com/resources/the-best-time-to-post-on-threads/)
- [Buffer — Best Content Format (45M posts)](https://buffer.com/resources/data-best-content-format-social-media/)

### Secondary Sources
- [Metricool — Threads Algorithm 2026](https://metricool.com/threads-algorithm/)
- [PostEverywhere — How the Threads Algorithm Works](https://posteverywhere.ai/blog/how-the-threads-algorithm-works)

---

> Built by [Allen](https://www.threads.net/@allenchiu0903) — a 52-year-old solo entrepreneur using AI to build systems that work while he sleeps.
> Original version created with [Nuwa Skill Builder](https://github.com/alchaincyf/nuwa-skill)
