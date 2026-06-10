# claude-code-builds

A growing collection of [Claude Code](https://claude.com/claude-code) skills I've built and use. Sharing in case they're useful to anyone else — fork and adapt.

Each skill is one `SKILL.md` file. Drop it into `~/.claude/skills/<skill-name>/` and Claude Code picks it up automatically. No build step, no install command.

---

## Skills

### `/blog-writer` — SEO + AEO + GEO + CRO content engine

Generates blog articles optimized across every modern discovery surface — Google, AI Overviews, ChatGPT, Perplexity, Claude, Gemini, Bing Copilot — with **lead generation as the primary success metric**, not traffic.

The skill is vertical-agnostic. On first run it asks for your brand, audience, voice, products, content inventory, and conversion model — so it works equally well for B2B SaaS, ecommerce, consumer apps, EdTech, professional services, or any vertical where lead generation is the metric. Once configured, every article goes through:

1. Intent classification (6 types, each with a tailored CTA strategy)
2. SERP feature targeting (9 features, including AI Overviews and PAA)
3. Competitor gap analysis (5-point framework)
4. Semantic keyword clustering (1 primary + 8–12 related)
5. Article draft with internal links, social proof, and conversion-ladder CTAs
6. Strategic output package: performance prediction, backlink targets, A/B tests, content lifecycle plan

Most "blog writer" prompts you find online stop at the draft. This one treats the article as a sales asset embedded in a longer lead-gen funnel.

**Requires:** nothing built-in. Works substantially better when you bring three CSVs: a linking inventory, GSC query export, and top-performer notes (the SKILL.md explains the schemas).

---

### `/social-listener` — daily social briefing

Multi-platform social listening, content ideation, and reputation monitoring. Produces a threaded Slack briefing every morning, aligned to your marketing calendar.

Sections (each posts as a separate thread reply for scannability):
- 📅 Today's calendar & what's going out
- 💡 Content ideas & growth opportunities (the primary deliverable, grouped by platform)
- 🔗 LinkedIn growth engine — opportunities + collab targets
- 🟡 Engagement opportunities — conversations to join
- 🟢 Competitor watch — actionable intel
- 🔴 Needs attention — only if genuinely urgent
- 📹 TikTok & YouTube — daily push on the underused channels
- 📊 Quick pulse — sentiment + counts

Vertical-agnostic. Configure once per brand (Slack channel, calendar, competitors, off-limits topics).

**Requires:** Claude Code with Slack and web search.

---

## Install

Pick a skill and drop the file into your local skills directory:

```bash
mkdir -p ~/.claude/skills/blog-writer
curl -o ~/.claude/skills/blog-writer/SKILL.md https://raw.githubusercontent.com/prtikku-ships/claude-code-builds/main/skills/blog-writer/SKILL.md
```

Replace `blog-writer` with `social-listener` for the other skill. Then open the file and fill in the Workspace Config section.

Restart Claude Code, type `/` to see the skill, and run it.

---

## License

MIT — do what you want, no warranty. Fork freely.
