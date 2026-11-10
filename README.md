# My Journey with Claude

Hands-on work from **The Complete Claude Code & Claude Cowork Masterclass (2026)** (Udemy) — every module I build, in one place.
Each module with practical output lives in its own self-contained folder under `modules/`.

## Projects
| Module | Project | Description | Folder |
|--------|---------|-------------|--------|
| 2 | [Gmail connector demo](modules/02-claude-cowork/gmail-connector-demo/) | Agent-built AI-in-healthcare proposal deck + 3-year cost workbook, sent through a Gmail connector, with a review of what the model got right and wrong | `modules/02-claude-cowork/gmail-connector-demo/` |

## Layout
```
.
├── README.md        # this index
├── COURSE.md        # module roadmap & progress tracker
├── logs/            # daily session logs (YYYY-MM-DD.md)
└── modules/
    └── NN-slug/     # one self-contained project per module, with its own README
```

## Conventions
- Each project folder is standalone: its own README, dependencies, and run instructions.
- Secrets go in `.env` (git-ignored); commit a `.env.example` instead.

## License
[Apache 2.0](LICENSE)
