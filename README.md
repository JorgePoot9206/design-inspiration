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

## File structure

```
design-inspiration/
├── .claude-plugin/
│   └── marketplace.json      # Marketplace metadata
├── skills/
│   └── design-inspiration/
│       ├── SKILL.md          # Main skill instructions
│       └── references/
│           └── categories.md # Full list of Awwwards categories, tags & tech filters
└── README.md
```

---

## Installation

### Claude Code — Marketplace
```bash
/plugin marketplace add JorgePoot9206/design-inspiration
```

### Claude Code — Manual
```bash
# Clone and copy skills directly
git clone https://github.com/JorgePoot9206/design-inspiration.git
cp -r design-inspiration/skills/* ~/.claude/skills/
```

---

## Design quality rules

The skill enforces these standards on every output:

- ✅ Always browses Awwwards **before** generating code — never works from memory alone
- ✅ Mentions at least **2 real Awwwards sites** as references
- ✅ Uses **CSS variables** for colors and typography
- ✅ Includes at least **one animation** or micro-interaction
- ✅ Fully **responsive**
- ❌ Never produces Bootstrap-looking or Wix-template-style designs

---

## Example output

> *"hazme una landing page para un sitio católico"*

Claude navigated to `awwwards.com/websites/social-responsibility/`, analyzed **OceanX 2025** (SOTD) and **Breakthrough Energy** (SOTD), extracted their design patterns, and generated a fully custom landing page with:

- Warm cream palette `#FAF7F2` + gold `#C9A84C`
- Cormorant Garamond editorial typography
- Asymmetric hero layout with floating cards
- Scroll-triggered fade animations
- Dark mission band with Bible quote

---

## Current design trends applied (2025–2026)

- Editorial serif typography at large scale
- Warm neutral backgrounds (cream, off-white)
- Two-color palettes with high contrast
- Asymmetric / broken grid layouts
- Scroll storytelling
- Minimal with one disruptive element
- Sticky nav with glassmorphism

---

## License

MIT — free to use, modify and share.
