# Neon — design reference

**Magenta and cyan on night**

One page showing every component in this design, rendered from its own design
tokens. No build step, no dependencies: open `index.html`.

**[View the component gallery →](https://mawentory.github.io/design-neon/)**

![Neon](preview.png)

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Component gallery — every component on one page |
| `DESIGN.md` | The design notes: origin, palette, type, shape, measured contrast |
| `theme.css` | The 66 design tokens, plus derived accessibility values |
| `design.css` | Component styles, written against tokens only |
| `fonts.css` | `@font-face` declarations for the fonts this design uses |
| `fonts/` | Latin-subset woff2 files, self-hosted |

`design.css` contains no colour, radius or font literal. That is deliberate: the
same stylesheet drives all ten designs and only `theme.css` differs, so the
gallery doubles as a test that the token set is complete.

## The design

Synthwave night: near-black violet, magenta and cyan light sources, and gradients that behave like illumination rather than decoration.

**Type** — Space Grotesk for display and body, IBM Plex Mono for data. The wide, geometric letterforms hold their own against the glow.

**Shape** — 1px borders, 12–26px radii, and soft coloured shadows that spill past the component edge like light on a wall.

**Signature moves**

- Radial gradient light sources fixed to the viewport.
- Signal-tinted shadows on cards and buttons.
- Cyan used for the mark while magenta leads the actions.

## Colour

| Token | Value | Role |
| --- | --- | --- |
| `--paper` | `#0b0620` | Page ground |
| `--sheet` | `#170d3a` | Raised surfaces |
| `--ink` | `#f4ecff` | Primary text |
| `--signal` | `#ff3ea5` | Action |
| `--signal-text` | `#ff3ea5` | Action, when it has to be read |
| `--focus-ring` | `#ff3ea5` | Focus indicator |

## Accessibility

Every colour pair this design can render as text is checked against WCAG 2.1
when the repo is generated — page surfaces, panel surfaces, and the tinted fills
of badges and diff lines. The full table is in
[DESIGN.md](DESIGN.md#contrast-measured); the gallery is separately audited in a
real browser for heading order, duplicate ids, unlabelled controls and
horizontal overflow at 1280px and 390px.

## Using it

Set the theme attribute on your root element and load the two stylesheets:

```html
<html data-theme="neon">
  <link rel="stylesheet" href="fonts.css" />
  <link rel="stylesheet" href="theme.css" />
  <link rel="stylesheet" href="design.css" />
</html>
```

Because the tokens are namespaced by attribute, this theme can sit alongside
another one in the same page.

## The rest of the set

[Placa](https://github.com/mawentory/design-placa), [Blueprint](https://github.com/mawentory/design-blueprint), [Phosphor](https://github.com/mawentory/design-fosforo), [Press](https://github.com/mawentory/design-imprensa), [Swiss](https://github.com/mawentory/design-suico), [Brutalist](https://github.com/mawentory/design-brutalista), [Botanical](https://github.com/mawentory/design-botanico), [Bauhaus](https://github.com/mawentory/design-bauhaus), [Vidro](https://github.com/mawentory/design-vidro).

---

Part of the MarvinRouter design set. Generated from a single template; see
`DESIGN.md` for the values behind it.
