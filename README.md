# Cold Email Quickstart

Workspace for cold email campaigns driven by the `cold-email-quickstart` Claude Code skill
(first-run wizard: sequencer signup → inboxes → strategy → lead tracking → scraping →
verification → copywriting → A/B testing → paused deploy).

- Skills live in `.claude/skills/`.
- Campaign state is written to `scripts/campaigns/<name>/.metadata.json` by the wizard.
- Dependency skills (lead-tracking-db, consulti-scrape, email-verification, inbox-insiders,
  list-optimize, cold-email-strategy, cold-email-copywriting, cold-email-ab-testing,
  cold-email-campaign-deploy) install via:

  ```bash
  curl -sSL 'https://leadgenjay.com/api/skills/install.sh?items=lead-tracking-db,list-optimize,consulti-scrape,email-verification,cold-email-campaign-deploy,cold-email-strategy,cold-email-copywriting,cold-email-ab-testing,inbox-insiders' | bash
  ```

Secrets go in `.env` (gitignored) — never commit API keys.
