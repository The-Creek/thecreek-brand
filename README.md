# The Creek Brand

This repository is the single source of truth for The Creek's brand assets and guidelines. It is designed to be consumed by staff, designers, and AI tools to produce consistently on-brand work.

## Repository Structure

| Path | Description |
|---|---|
| `brand-kit.json` | Machine-readable brand data — colors, typography, logos, sub-brands, voice, and rules |
| `brand-guidelines.md` | Human and agent-readable guidelines — tone, logo usage, writing standards, and terminology |
| `index.html` | Visual reference page for all brand assets |
| `fonts/` | Self-hosted font files — Gotham Bold, Bebas Neue Pro, Avenir, Portrait Script |
| `logos/` | The Creek logo lockups — combination marks (horizontal and stacked), logo mark, and secondary variants |
| `ministries/` | Ministry sub-brand logo assets |
| `guidelines/` | Official brand style guide PDFs |

## brand-kit.json Structure

```json
{
  "version": "2026.06",

  "brand": {
    // Legal name (Indian Creek Christian Church), brand name (The Creek), website
  },

  "locations": [
    // Primary campus: 6430 S Franklin Rd, Indianapolis, IN 46259
    // Each entry: type, street, city, state, zip, country, lat, lng
  ],

  "color_system": {
    "palette": {
      "primary":   // Black (#231F20) — main brand color, RGB, CMYK, text_on
      "secondary": // White (#FFFFFF) — co-primary, logo reversal and backgrounds
      "neutrals":  // Dark Gray (#6D6E71, Pantone 424 C) and Medium Gray (#A7A9AC, Pantone 7543 C)
      "accents":   // Nepal (#95B1C1), Solid Pink (#984445), Patina (#598D7F), Tan Hide (#F79A70)
                   // Each with Pantone reference and text_on value
    },
    "interface": {
      // 5-step neutral scale: softest → strongest
      // Inverts symmetrically in dark mode
    },
    "semantic": {
      // success, warning, danger, info
      // Each has forecolor and background with light/dark values
    }
  },

  "typography": {
    "primary":   // Gotham Bold — headlines and CTAs, self-hosted OTF
    "secondary": // Bebas Neue Pro — subheadings, self-hosted TTF
    "body":      // Avenir — body copy, upper/lowercase only, self-hosted TTF
    "accent":    // Portrait Script — decorative only, never for readable copy, self-hosted TTF
  },

  "logos": {
    "lockups": [
      // Array of logo lockup entries, each identified by type:
      // combination_mark_horizontal — icon + wordmark, horizontal (primary/preferred)
      // combination_mark_stacked    — icon + wordmark, stacked (space-constrained contexts)
      // logo_mark                   — icon only (avatars, favicons, small spaces)
      // secondary_horizontal        — alternate variant, horizontal
      // secondary_stacked           — alternate variant, stacked
      // Each lockup contains an assets[] array with dark and light PNG variants
    ],
    "rules": [
      // Logo usage rules for agents and designers
    ]
  },

  "sub_brands": [
    // Array of ministry sub-brand entries, each with:
    //   id, type ("ministry"), name, full_name, accent_color, logos.assets[]
    //
    // life-groups         — Teal (#598D7F, Pantone 625 C)
    // marriage-parenting  — Aqua (#9ECDC9)
    // mens-formation      — Olive (#919373)
    // womens-formation    — Blush (#D9ACA3)
    // outreach            — Orange (#F89B49)
    // safety-security     — Silver (#CED1D0)
    // special-needs       — Yellow (#F8D982)
    //
    // Each ministry has combination_mark and wordmark assets in dark and light variants
  ],

  "voice": {
    // summary, tone descriptors, language to avoid
  },

  "rules": [
    // Top-level agent directives for using this brand kit
  ]
}
```

## Asset Conventions

**Variants:** Every asset entry includes a `variant` field — `dark` (black logo, for light backgrounds) or `light` (white logo, for dark backgrounds).

**Format:** All logo assets are PNG with transparent backgrounds.

**File paths:** All paths are relative to the repository root and match the physical directory structure.

**Logo usage:** Always prefer the horizontal combination mark. Use stacked only when horizontal space is limited. Use the logo mark only for avatars, favicons, or where the full brand is already established in context. Logos are black or white only — no recoloring.

**Ministry logos:** For external-facing materials, pair ministry logos with The Creek logo mark. For internal communications, The Creek logo mark is optional. When in doubt, include it.
