# LinkedIn post skill demo: "The state of AI in 2025"

**Module 2: Agent Skills practical demo.** Install a community skill from a skills directory and use it on a real document: turn McKinsey/QuantumBlack's *The state of AI in 2025* into a LinkedIn post.

| | |
|---|---|
| Agent | Freebuff |
| Skill | [`linkedin-post-writer`](https://www.skills.sh/social-media-skills/skills/linkedin-post-writer) by social-media-skills (skills.sh) |
| Source | [The state of AI in 2025: Agents, innovation, and transformation](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai) (McKinsey / QuantumBlack, November 2025) |
| Date | 2026-11-13 |

The PDF is kept locally only (git-ignored): it's McKinsey's copyrighted report, so this repo links to it instead of republishing it.

## Skill directories explored
- [skills.sh](https://www.skills.sh): Vercel's directory; one-line install with `npx skills add`, shows install counts and security audits.
- [skillhub.club](https://skillhub.club)
- [skills.mp](https://skills.mp)
- [anthropics/skills](https://github.com/anthropics/skills): Anthropic's official skills on GitHub.

## Why this skill
| Candidate | Installs | Notes |
|---|---|---|
| `social-media-skills/linkedin-post-writer` | 1.1K | Picked. Passes all three security audits. Gives 2–3 post options and recommends one, puts links in the first comment, avoids engagement bait. |
| `inklate/linkedin-post` | 2 | Similar idea, barely used. |
| `acedatacloud/linkedin` | — | Calls the LinkedIn API; publishes rather than writes. Not what's needed. |

```bash
npx skills add https://github.com/social-media-skills/skills --skill linkedin-post-writer
```

## Report: key findings (for checking the post)
1. Nearly two-thirds of organizations have not begun scaling AI across the enterprise.
2. 62% are at least experimenting with AI agents.
3. 88% use AI in at least one business function (78% a year earlier), but only 39% report enterprise-level EBIT impact; 64% say AI enables innovation.
4. 80% set efficiency as an AI objective; high performers add growth and innovation goals.
5. Redesigning workflows is a key success factor for high performers.
6. Workforce outlook for the next year: 32% expect decreases, 43% no change, 13% increases.

## Result
_To be filled in after the run: the post(s) generated, which one was chosen, and a fact-check against the findings above._
