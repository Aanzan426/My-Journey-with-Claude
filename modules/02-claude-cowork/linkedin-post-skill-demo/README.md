# LinkedIn post skill demo: "The state of AI in 2025"

**Module 2: Agent Skills practical demo.** Install a community skill from a skills directory and use it on a real document: turn McKinsey/QuantumBlack's *The state of AI in 2025* into a LinkedIn post.

| | |
|---|---|
| Agent | Freebuff |
| Skill | [`linkedin-post`](https://www.skillhub.club/skills/different-ai-zero-finance-linkedin-post) by different-ai (from their [zero-finance](https://github.com/different-ai/zero-finance) repo), found on skillhub.club |
| Source | [The state of AI in 2025: Agents, innovation, and transformation](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai) (McKinsey / QuantumBlack, November 2025) |
| Date | 2026-11-13 |

The PDF is kept locally only (git-ignored): it's McKinsey's copyrighted report, so this repo links to it instead of republishing it.

## Skill directories explored
- [skills.sh](https://www.skills.sh): Vercel's directory; one-line install with `npx skills add`, shows install counts and security audits.
- [skillhub.club](https://skillhub.club)
- [skills.mp](https://skills.mp)
- [anthropics/skills](https://github.com/anthropics/skills): Anthropic's official skills on GitHub.

## The skill
[`SKILL.md`](https://github.com/different-ai/zero-finance/blob/main/.opencode/skill/linkedin-post/SKILL.md) (MIT). SkillHub AI score 8.4/10; its automated security review expired on 2026-06-27.

It's an in-house skill from a fintech startup (0 Finance), not a general-purpose one:
- **Reusable parts:** a post structure (hook → context → insight → proof → soft CTA), three templates (video teaser, product demo, behind-the-scenes), a pre-posting checklist, and anti-patterns to avoid (corporate announcements, feature dumps, humble brags).
- **Company-specific parts that won't apply here:** steps 1–2 search the company's private Notion "Tweet Lab" and marketing-audit pages through a Notion connector; neither is accessible, so the agent should skip them. The compliance section is about SEC rules for crypto-yield wording.
- **Mismatch to watch:** its templates are built around showing off a product demo, while this input is a research report. The "behind-the-scenes" or a data-led "bold claim" structure fits a report best.

Alternatives considered on skills.sh: `social-media-skills/linkedin-post-writer` (1.1K installs, more general), `inklate/linkedin-post` (2 installs), `acedatacloud/linkedin` (publishes through the LinkedIn API instead of writing).

## Report: key findings (for checking the post)
1. Nearly two-thirds of organizations have not begun scaling AI across the enterprise.
2. 62% are at least experimenting with AI agents.
3. 88% use AI in at least one business function (78% a year earlier), but only 39% report enterprise-level EBIT impact; 64% say AI enables innovation.
4. 80% set efficiency as an AI objective; high performers add growth and innovation goals.
5. Redesigning workflows is a key success factor for high performers.
6. Workforce outlook for the next year: 32% expect decreases, 43% no change, 13% increases.

## Result
_To be filled in after the run: the post(s) generated, which one was chosen, and a fact-check against the findings above._
