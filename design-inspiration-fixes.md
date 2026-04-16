# Fixes para design-inspiration skill

Estos son los cambios necesarios para que el skill se pueda instalar correctamente
desde el marketplace de Claude Code (`/plugin marketplace add`).

---

## Problema

El repo le falta el archivo `.claude-plugin/marketplace.json`.
Sin este archivo, Claude Code no sabe cómo registrar el skill al instalarlo.

---

## Cambio 1 — Mover el SKILL.md a la estructura estándar

La convención oficial de Anthropic es:

```
skills/
  design-inspiration/
    SKILL.md
    references/
      categories.md
```

**Qué hacer:**

```bash
mkdir -p skills/design-inspiration
mv design-inspiration/SKILL.md skills/design-inspiration/SKILL.md
mv design-inspiration/references skills/design-inspiration/references
rmdir design-inspiration
```

---

## Cambio 2 — Crear el archivo `.claude-plugin/marketplace.json`

Este archivo es el que hace funcionar `/plugin marketplace add`.

**Qué hacer:**

```bash
mkdir -p .claude-plugin
```

Crear el archivo `.claude-plugin/marketplace.json` con este contenido:

```json
{
  "name": "design-inspiration-skills",
  "version": "1.0.0",
  "description": "Genera diseños web originales consultando Awwwards como fuente de inspiración",
  "author": "JorgePoot9206",
  "plugins": [
    {
      "name": "design-inspiration",
      "description": "Generate inspired web designs by researching Awwwards award-winning sites before coding",
      "source": "./",
      "skills": ["design-inspiration"],
      "strict": false
    }
  ]
}
```

---

## Estructura final del repo

Después de los cambios, el repo debe verse así:

```
design-inspiration/           <- raíz del repo en GitHub
├── .claude-plugin/
│   └── marketplace.json      <- NUEVO
├── skills/
│   └── design-inspiration/   <- MOVIDO
│       ├── SKILL.md
│       └── references/
│           └── categories.md
├── .gitattributes
└── README.md
```

---

## Cambio 3 — Eliminar `.claude/settings.local.json` del repo

El archivo `.claude/settings.local.json` es configuración local y no debe estar
en el repositorio público. Agrégalo al `.gitignore`:

```bash
echo ".claude/" >> .gitignore
git rm --cached .claude/settings.local.json
```

---

## Instalación después de los cambios

Una vez pusheados los cambios a GitHub, el skill se instala así:

```bash
/plugin marketplace add JorgePoot9206/design-inspiration
/plugin install design-inspiration@JorgePoot9206
```

O con GitHub directo:

```bash
claude plugin install https://github.com/JorgePoot9206/design-inspiration
```

O manual (sin marketplace):

```bash
cp -r ./skills/* ~/.claude/skills/
```
