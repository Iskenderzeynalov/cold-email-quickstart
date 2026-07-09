# Cold Email Skills — Which One At Which Stage

A map of the installed skills to the cold-email workflow, from list to send.
Invoke any skill with `/<name>` in Claude Code.

## Installed skills

| Skill | Job | Backed by |
|-------|-----|-----------|
| `vibe-prospecting` | Find & enrich leads, research accounts | Explorium (150M+ companies, 800M+ people, verified) |
| `cold-email` | Write emails + follow-up sequences | Corey Haines' copy rules (human, not template) |
| `self-critique` | Score a draft & rework until it clears a quality bar | local loop skill |
| `cold-email-quickstart` | End-to-end wizard (optional orchestrator) | leadgenjay (dependencies not installed) |

## Stage-by-stage

| # | Stage | Use | Notes |
|---|-------|-----|-------|
| 1 | **Strategy / ICP** | *(your notes / cold-email-quickstart Phase 3)* | Define who you target and the offer before touching data. |
| 2 | **Build lead list** | `vibe-prospecting` | Search companies + contacts by ICP filters. Verified data = no hallucinated personalization. |
| 3 | **Research / enrich** | `vibe-prospecting` | Pull tech stack, business events, website changes, intent — the raw material for real personalization. |
| 4 | **Verify emails** | *(Instantly MCP — connected)* | Get bounce rate under ~3% before sending. Use Instantly's verification. |
| 5 | **Write copy** | `cold-email` | Subject lines, openers, body, CTAs, multi-touch follow-ups. Auto-loads product context if present. |
| 6 | **Refine copy** | `self-critique` | Layer on top of #5 output: critiques the draft and reworks it up to an explicit bar (default 4 rounds). |
| 7 | **A/B variants** | `cold-email` (variants) + `self-critique` | Generate multiple variants, then score each. |
| 8 | **Deploy (paused)** | *(Instantly MCP — connected)* | Create campaign, load sequence + leads, keep PAUSED. Warm domains 4+ weeks before activating. |
| 9 | **Monitor** | *(Instantly MCP — connected)* | Track opens/replies/bounces; re-verify list if >30 days pass before send. |

## Recommended chain
`vibe-prospecting` (lead + research) → Instantly verify → `cold-email` (write) → `self-critique` (polish) → Instantly (deploy paused) → warmup → activate.

## Reminders
- A skill makes output consistent — it won't fix a weak offer, dirty list, or cold domains. Infra + warmup still matter.
- Skills run with full agent permissions; review before use.
- Secrets live in `.env` (gitignored). Never commit API keys.
