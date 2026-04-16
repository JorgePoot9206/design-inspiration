---
name: design-inspiration
description: >
  Genera diseños web originales e inspirados consultando Awwwards.com por categoría. Usa este skill
  SIEMPRE que el usuario pida: inspiración de diseño web, generar un diseño o componente UI, crear
  una landing page, portafolio, e-commerce, o cualquier interfaz web. También úsalo cuando el usuario
  mencione tendencias de diseño, animaciones web, tipografía, colores, o pida ejemplos visuales de
  buenas prácticas de UX/UI. Si el usuario dice "hazme un diseño", "quiero inspiración", "diseña como
  [industria]", "genera un componente con buen diseño", "crea una web para [tipo de negocio)", este
  skill es OBLIGATORIO. Navega Awwwards por la categoría más relevante, analiza los sitios ganadores,
  extrae patrones de diseño, y genera código HTML/CSS/React original e inspirado en esas tendencias.
---

# Awwwards Design Inspiration Skill

Genera diseños web originales consultando Awwwards.com como fuente de inspiración real y actualizada.

## Flujo de trabajo

### Paso 1 — Identificar la categoría correcta

Mapea el tipo de proyecto del usuario a una categoría de Awwwards:

| Tipo de proyecto | URL de Awwwards |
|---|---|
| E-commerce / Tienda | `https://www.awwwards.com/websites/e-commerce/` |
| Portafolio / Agencia | `https://www.awwwards.com/websites/portfolio/` |
| Arquitectura / Inmobiliaria | `https://www.awwwards.com/websites/architecture/` |
| Restaurant / Hotel | `https://www.awwwards.com/websites/hotel-restaurant/` |
| Moda / Lujo | `https://www.awwwards.com/websites/fashion/` |
| Startup / Tech | `https://www.awwwards.com/websites/startups/` |
| Arte / Ilustración | `https://www.awwwards.com/websites/art-illustration/` |
| Agencia de Diseño | `https://www.awwwards.com/websites/design-agencies/` |
| Corporativo / Negocios | `https://www.awwwards.com/websites/business-corporate/` |
| Experimental / Interactivo | `https://www.awwwards.com/websites/experimental/` |
| Fotografía | `https://www.awwwards.com/websites/photography/` |
| Música / Sonido | `https://www.awwwards.com/websites/music-sound/` |
| Comida / Bebida | `https://www.awwwards.com/websites/food-drink/` |
| Juegos / Entretenimiento | `https://www.awwwards.com/websites/games-entertainment/` |
| Deportes | `https://www.awwwards.com/websites/sports/` |
| Lujo | `https://www.awwwards.com/websites/luxury/` |
| Animación / Motion | `https://www.awwwards.com/websites/animation/` |
| 3D / WebGL | `https://www.awwwards.com/websites/3d/` |
| Tipografía | `https://www.awwwards.com/websites/typography/` |
| Minimal / Limpio | `https://www.awwwards.com/websites/minimal/` |
| Colorido | `https://www.awwwards.com/websites/colorful/` |

Si no hay coincidencia clara, usar Sites of the Day: `https://www.awwwards.com/websites/sites_of_the_day/`

### Paso 2 — Navegar Awwwards y analizar sitios

1. Usa `web_fetch` en la URL de la categoría correspondiente
2. Extrae los nombres de los sitios listados (ganadores, nominees, SOTD)
3. Visita al menos **2-3 páginas de detalle** de sitios con premios (SOTD, HM) usando sus URLs: `https://www.awwwards.com/sites/[slug-del-sitio]`
4. Para cada sitio analizado, anota:
   - **Paleta de colores** (fondo, primarios, acentos)
   - **Tipografía** (familias, pesos, tamaños, jerarquía)
   - **Layout** (grid, espaciado, proporciones)
   - **Animaciones / interacciones** mencionadas
   - **Elementos visuales** únicos (formas, texturas, imágenes)
   - **Navegación** (menú, scroll, transiciones)

### Paso 3 — Sintetizar patrones de diseño

Antes de generar código, resume internamente:
- ¿Qué tienen en común los mejores diseños de esta categoría?
- ¿Qué hace que sean originales y no genéricos?
- ¿Qué tendencias actuales (2025-2026) se ven?

Tendencias actuales frecuentes en Awwwards:
- **Tipografía como elemento visual** (texto gigante, variable fonts)
- **Fondos oscuros con acentos neón o tierra**
- **Microinteracciones y cursores personalizados**
- **Layouts asimétricos y grids rotos**
- **Imágenes a sangre + texto superpuesto**
- **Scrollytelling y animaciones al hacer scroll**
- **Estética "editorial" (inspirada en revistas)**
- **Minimalismo con un elemento disruptivo**
- **Gradientes granulados / ruido**

### Paso 4 — Generar el diseño

Produce código HTML/CSS (o React/JSX si el usuario lo pide) que:

1. **Sea original**, no una copia de ningún sitio visitado
2. **Refleje patrones reales** extraídos del análisis
3. **Incluya comentarios** explicando decisiones de diseño
4. **Sea funcional y responsivo**
5. **Use variables CSS** para colores y tipografía
6. **Tenga al menos una animación** o micro-interacción notable

### Paso 5 — Presentar con contexto

Al entregar el diseño, incluye:
- **Fuentes de inspiración**: menciona los sitios de Awwwards que más influyeron
- **Decisiones de diseño**: explica brevemente las elecciones clave (paleta, tipografía, layout)
- **Tendencias aplicadas**: nombra qué tendencias actuales se usaron
- **Cómo personalizarlo**: sugiere variaciones o ajustes posibles

---

## Reglas de calidad

- **Nunca generar diseños genéricos o "de plantilla"**. Si el resultado se parece a Bootstrap o a un template de Wix, es una falla.
- **Siempre navegar Awwwards primero** antes de generar código. No trabajar desde memoria.
- **Mencionar al menos 2 sitios reales** de Awwwards como referencia de inspiración.
- El código debe poder ejecutarse directamente en un browser o en el artifact viewer de Claude.
- Para componentes React, usar Tailwind para utilidades y CSS custom para efectos especiales.

---

## Referencia de filtros útiles de Awwwards

Para afinar la búsqueda puedes combinar categoría + tag:
- Minimal + categoría: añadir `/minimal/` al filtro
- Solo ganadores SOTD: `https://www.awwwards.com/websites/sites_of_the_day/`
- Por tecnología (ej. Webflow): `https://www.awwwards.com/websites/webflow/`
- Más votados del mes: `https://www.awwwards.com/websites/sites_of_the_month/`

Ver `references/categories.md` para la lista completa de categorías y tags disponibles.
