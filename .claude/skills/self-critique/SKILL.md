---
name: self-critique
description: "Iteratively critique and rework any draft output until it clears an explicit quality bar. Use when the user says 'make this better', 'critique and improve', 'self-review', 'refine until good', 'iterate on this', or asks for the highest-quality version of copy, emails, or written output. Works well layered on top of cold-email or any writing skill."
---

# Self-Critique — Iterative Refinement Loop

A quality amplifier you layer on TOP of another skill's output (e.g. `cold-email`).
Do NOT generate the first draft here — take an existing draft and drive it up to a bar.

## Loop

1. **Set the bar.** State 3–6 explicit, testable criteria BEFORE scoring. For cold email, default to:
   - Sounds like one sharp human, not a template
   - Subject line ≤5 words, no spammy words, sparks curiosity
   - Opening line is about THEM, not "I/we/our"
   - One clear ask, one idea per email
   - Under ~90 words, reads in one breath
   - No unverifiable claims / hallucinated personalization
   If the user gave their own criteria, use those instead.

2. **Score the current draft** against each criterion: PASS / WEAK / FAIL with a one-line reason each. Be a harsh critic — assume the reader is busy and skeptical.

3. **Stop or continue:**
   - If every criterion is PASS (or you've hit the iteration cap, default 4) → output the final version + the final scorecard. STOP.
   - Otherwise → rewrite the draft fixing every WEAK/FAIL, then go back to step 2.

4. **Never loop silently.** Show each round compactly: `Round N: <one-line what changed>` + the scorecard. The user should see the draft improve.

## Rules
- Attack the draft, not defend it. Each round must find something real to fix until it genuinely can't.
- Preserve any verified facts; never invent new personalization to "improve" a line.
- Default cap: 4 rounds. Raise only if the user asks. Announce the cap up front.
- If the draft is already excellent, say so in one round — don't manufacture churn.
