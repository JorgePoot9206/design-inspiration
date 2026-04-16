# Design Inspiration Skill

A skill for Claude that generates original, high-quality web designs by browsing [Awwwards.com](https://www.awwwards.com) for real inspiration before writing any code.

---

## What it does

Instead of generating generic, template-looking designs, this skill:

1. **Navigates Awwwards** by the most relevant category for your project
2. **Analyzes award-winning sites** (Site of the Day, Honorable Mentions) — extracting color palettes, typography, layout patterns, and interactions
3. **Synthesizes current trends** (2025–2026) from the best designers in the world
4. **Generates original code** (HTML/CSS or React) inspired by those real references — never a copy

---

## Installation

### Claude Code — Marketplace
```bash
#install the skill
/plugin install design-inspiration@JorgePoot9206
```

---

## Triggers

Use this skill whenever you ask Claude things like:

- *"hazme una landing page para..."*
- *"quiero inspiración para un diseño de..."*
- *"diseña una web para [tipo de negocio]"*
- *"crea un componente con buen diseño"*
- *"generate a UI for..."*
- *"I need a website design for..."*

---

## Categories supported

The skill maps your project to the right Awwwards category automatically:

| Project type | Awwwards category |
|---|---|
| Online store | E-commerce |
| Portfolio / Agency | Portfolio |
| Restaurant / Hotel | Hotel & Restaurant |
| Fashion / Luxury | Fashion / Luxury |
| Startup / Tech | Startups / Technology |
| Architecture | Architecture |
| Art / Illustration | Art & Illustration |
| Corporate | Business & Corporate |
| Food & Drink | Food & Drink |
| Photography | Photography |
| Events | Events |
| Music | Music & Sound |
| Sports | Sports |
| Experimental / Interactive | Experimental |
| + many more | See `references/categories.md` |

---


## License

MIT — free to use, modify and share.
