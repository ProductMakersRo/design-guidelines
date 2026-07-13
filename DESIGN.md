---
name: Product Makers
description: "A well-typeset makers' zine — black display type on warm paper, two loud paint colors, and tilted highlighter-marker labels. Confident, hand-made, never templated."
colors:
  ink: "#191919"
  ink-2: "#3f3f46"
  mute: "#656c7a"
  paper: "#fdfdfd"
  surface: "#ffffff"
  surface-2: "#f3f4f7"
  line: "#dcdde1"
  blue: "#3f3fff"
  blue-press: "#2d2de0"
  blue-soft: "#e8e8ff"
  blue-bright: "#5555ff"
  blue-glow: "#6f6fff"
  orange: "#ff5500"
  primary: "#cc4600" # the CTA color; realized as --primary in globals.css, not a separate --pm-orange-cta var
  orange-press: "#b03d00"
  orange-soft: "#ffe4d6"
  yellow-100: "#fcf300"
  lime-100: "#d3ff33"
  green-100: "#9fff3f"
  lavender-100: "#ebeefc"
  spring-100: "#3fff9f"
  tag-shadow-yellow: "#c9c200"
  tag-shadow-lime: "#a6cc1f"
  tag-shadow-green: "#75c91e"
  tag-shadow-white: "#cfd4e5"
  success: "#16a34a"
  warning: "#f59e0b"
  error: "#dc2626"
typography:
  display:
    fontFamily: "Noto Sans Display, Noto Sans, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 5vw, 4.5rem)"
    fontWeight: 900
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Noto Sans Display, Noto Sans, system-ui, sans-serif"
    fontSize: "clamp(1.875rem, 4vw, 3.75rem)"
    fontWeight: 900
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Noto Sans Display, Noto Sans, system-ui, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 900
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Noto Sans, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Noto Sans, system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
  caption:
    fontFamily: "JetBrains Mono, ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.15em"
rounded:
  sm: "6px"
  md: "8px"
  lg: "12px"
  xl: "16px"
  2xl: "20px"
  3xl: "28px"
  4xl: "32px"
  pill: "9999px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  section-y: "64px"
  section-y-lg: "96px"
  container: "1280px"
components:
  button-primary:
    backgroundColor: "{colors.orange}"
    textColor: "#ffffff"
    rounded: "{rounded.lg}"
    padding: "10px 24px"
    typography: "{typography.label}"
  button-primary-hover:
    backgroundColor: "{colors.orange-press}"
    textColor: "#ffffff"
  button-primary-lg:
    backgroundColor: "{colors.orange}"
    textColor: "#ffffff"
    rounded: "{rounded.lg}"
    padding: "12px 32px"
  button-outline:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "10px 24px"
  button-ghost:
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "10px 16px"
  highlight-tag:
    backgroundColor: "{colors.yellow-100}"
    textColor: "{colors.ink}"
    rounded: "14px"
    padding: "10px 22px"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.3xl}"
    padding: "28px"
  meta-pill:
    backgroundColor: "{colors.surface-2}"
    textColor: "{colors.ink-2}"
    rounded: "{rounded.pill}"
    padding: "4px 12px"
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.lg}"
    padding: "8px 12px"
---

# Design System: Product Makers

## 1. Overview

**Creative North Star: "The Makers' Zine."**

Product Makers is a well-typeset zine made by makers, rebuilt as a website. The
register is **brand**: this is a community marketing site, so the design *is* the
product. The whole system runs on three physical-object words from the brand
brief: **hand-lettered, loud, document-like.** Confident black display type on
warm off-white paper. Two loud brand colors used as *paint*, never decoration.
And the signature move: tilted highlighter-marker labels that look drawn on by
hand. It must feel made by a person, not generated.

Structure is done with **1px ink-tinted rules, not shadows** — the page reads
like a well-set document, columns and dividers doing the work, whitespace giving
it air. Loudness is rationed: the blue drenched hero and the single orange CTA
are the set-pieces; everything between them is quiet ink-on-paper so the loud
moments actually land. The voice matches the look: welcoming, second-person,
Slack-fluent, quietly confident. Sentence case everywhere, buttons are 1 to 3
word imperatives ("Join on #Slack"), and free is the headline, not the footnote.

This system explicitly rejects: **generic SaaS landing pages** (cream + Inter +
gradient-text hero + big-number stat row + identical icon-heading-text card
grid); the **editorial-magazine AI lane** (display-serif italic + tiny tracked
uppercase kickers over every section + ruled columns); **crypto/neon-on-black**;
and anything that reads "AI made that."

**Key Characteristics:**
- **Instantly recognizable by:** tilted highlighter labels with a hard bottom shadow · black Noto Sans Display on warm paper · blue `#3f3fff` identity + orange `#ff5500` action · blue text-selection · borders instead of shadows.
- **Committed** on brand set-pieces (blue drenched hero, orange CTA), **Restrained** on content (ink on paper, hairline rules).
- One conversion per screen; **Grow / Build / Connect** is the routing spine.
- Real faces and names over abstract graphics — the community is the product.
- No dark mode (deliberately undefined), no script/cursive face, no gradients on chrome.

## 2. Colors

Warm off-white paper and deep ink, two loud brand colors held in strict roles,
plus a five-hue highlighter cast reserved for the tilted labels and small chips.
Canonical values are hex (as defined in `src/app/globals.css`); every brand
token is namespaced `pm-*`.

### Primary
- **Identity Blue** (`#3f3fff`, `pm-blue`): the brand's identity paint. The logo, every focus ring (`--ring`), the master-hero field, `HighlightTag`-adjacent fills, text selection. Press `#2d2de0`, soft wash `#e8e8ff`, bright gradient-start `#5555ff`, glow blob `#6f6fff`. **Never a CTA fill. Never a text color.**
- **Action Orange** (`#ff5500`, `pm-orange`): the conversion paint, decorative accents only. The CTA *fill* is the darkened `#cc4600` (`--primary`) — AA contrast (4.7:1) with its white label; same 20° hue. Hover/press `#b03d00`, soft tint `#ffe4d6` for rare backgrounds. At most one orange element per screen.

### Secondary — the Highlighter Cast
Five hues, only ever as `HighlightTag` fills and small categorical chips. Each
ships as 100 (full) / 60 (mid) / 40 (washed) tints; the 100 is the working value.
- **Yellow** (`#fcf300`) · **Lime** (`#d3ff33`) · **Green** (`#9fff3f`) · **Lavender** (`#ebeefc`) · **Spring** (`#3fff9f`).
- Each tag carries a **hard 4px bottom shadow in a darker tone of its own fill, never black**: yellow→`#c9c200`, lime→`#a6cc1f`, green→`#75c91e`, white/lavender→`#cfd4e5`.

### Neutral
- **Ink** (`#191919`, `pm-ink`): all primary text, dark bands, the darkest surfaces.
- **Ink-2** (`#3f3f46`): secondary body text, descriptions.
- **Mute** (`#656c7a`): captions, meta, disabled, roles under names. Darkened from `#9ca3af` for AA contrast (≥4.5:1 on paper, white and surface-2).
- **Paper** (`#fdfdfd`): the default page background — warm off-white, never pure white for the canvas.
- **Surface** (`#ffffff`): cards and raised panels sit one step brighter than paper.
- **Surface-2** (`#f3f4f7`): insets, meta pills, alternating section bands, hover tints.
- **Line** (`#dcdde1`): every 1px border and divider — the structural workhorse.

### Semantic (rare, UI-only)
- **Success** `#16a34a` · **Warning** `#f59e0b` · **Error** `#dc2626`. Utility states only; not part of the marketing palette.

### Named Rules
**The Two-Paint Rule.** Blue is identity, orange is action, and they never swap. Blue never fills a CTA; orange never fills anything but the one conversion button per screen.

**The No-Colored-Text Rule.** Text is ink (or its opacity steps) on light, white (or white/opacity) on dark. Blue, orange and the highlighter cast are paint — fills for buttons, tags, canvases, focus rings, the logo — **never applied to text** for emphasis or as a link color. Emphasis is weight and size; a link is weight + underline or an arrow, never a hue.

**The Rationed-Loud Rule.** Saturated color carries the hero and the CTA and stops there. On any content screen the loud colors sit near 10% of the surface; their rarity is what makes them read as loud.

## 3. Typography

**Display Font:** Noto Sans Display (fallback Noto Sans, system-ui)
**Body / UI Font:** Noto Sans (fallback system-ui) — 400–900, latin-ext for Romanian diacritics
**Spec / Mono Font:** JetBrains Mono — dates, stat captions, spec labels

**Character:** One humanist sans does almost all the work, black and tight at the
top of the scale for a confident, hand-set-poster feel, relaxed and readable in
body. There is **no script or cursive face anywhere** — the hand-lettered
"Makers" wordmark exists only as an SVG logo asset, never as type. Emphasis is
always weight, never a special face and never color.

### Hierarchy
- **Display** (900, `clamp(2.25rem → 4.5rem)`, line-height 1.02, tracking -0.02em): hero H1 only. `text-balance` splits the lines that are needed.
- **Headline** (900, `clamp(1.875rem → 3.75rem)`, line-height 1.05, tracking -0.02em): section H2.
- **Title** (900, ~1.5rem, line-height 1.15, tracking -0.01em): card and item H3.
- **Body** (400, 1–1.125rem, line-height ~1.6, cap length 65–75ch): paragraphs; weight 500/700 for inline emphasis.
- **Label** (700–800, 0.75–0.875rem): buttons, pills, names, UI. Sentence case.
- **Caption / spec** (JetBrains Mono, 500, 0.75rem, letter-spacing 0.15em, uppercase): dates, stat captions, the "00 / GLOBAL NAVBAR" device. This is the *only* sanctioned uppercase-tracked treatment, and it never sits over a title as a kicker.

### Named Rules
**The Sentence-Case Rule.** Everything is sentence case: headings, buttons, labels, nav. No ALL-CAPS marketing shouts. The one exception is the mono spec caption above.

**The Weight-Not-Color Rule.** Hierarchy comes from scale + weight (≥1.25 step ratio between levels) and nothing else. Never lighten, tint, or color a word to rank it.

**The Titles-Use-Available-Width Rule.** A heading breaks to a second line only when it genuinely does not fit, never because a container is capped too tight. Give display titles a wide cap (`max-w-5xl`) so a short line like "Ten tracks, led by people who ship." stays on one line. Left-aligned section leads use `max-w-4xl` (not `max-w-2xl`) so descriptions fill the width instead of cramming into a narrow column under a wide title; centered leads may stay `max-w-2xl`.

## 4. Elevation

Depth is built with **borders and tonal layering, not shadows.** A 1px `#dcdde1`
rule is the primary tool for separating and grouping; surfaces step in tone
(paper → surface → surface-2) to signal layer. The shadow scale exists but is a
whisper, reserved for genuinely floating elements and hover state — never for
resting structure.

### Shadow Vocabulary
- **sm** (`0 1px 2px rgb(0 0 0 / 0.05)`): the resting lift under the primary CTA and small raised chips. Barely there.
- **md** (`0 4px 12px rgb(25 25 25 / 0.06)`): hover state on cards, dropdowns, popovers.
- **lg** (`0 12px 32px rgb(25 25 25 / 0.08)`): truly floating set-pieces (the program overview card, modals).
- Signature accents carry their own **hard offset shadow** (the `HighlightTag`'s `0 4px 0 0` in a darker fill tone) — a graphic device, not elevation.

### Named Rules
**The Borders-Not-Shadows Rule.** Structure is drawn with 1px rules and tonal steps. If a layout needs a shadow to feel organized, the border and spacing are wrong first. Shadows appear only as a response to state (hover, float, focus), never at rest on a content card.

**The No-Glass Rule.** No glassmorphism, no backdrop-blur cards, no glow, no neon. Gradients live *only* inside sanctioned hero/canvas set-pieces (the blue master hero, page headers), never on chrome, buttons, or content cards.

## 5. Components

### Buttons
- **Shape:** 12px corners (`rounded-lg`), 700-weight sentence-case label, 150ms color transitions, no transform on press. Focus ring is always brand blue: `focus-visible` grows a 3px `blue/20` ring plus a blue border.
- **Primary (the CTA):** solid orange (`#cc4600`, `--primary` — AA contrast with the white label) fill, white text, faint `sm` shadow; hover deepens to `#b03d00`. Padding `10px 24px` (default) or `12px 32px` (`lg`). **At most one per screen**, for the conversion.
- **Outline (the workhorse):** transparent/surface fill, `line` border, ink text; hover fills with `surface-2`. This carries every secondary action.
- **Ghost:** text-only ink label, hover shows a subtle `surface-2` tint (never colored text); tighter `10px 16px` padding.
- **Link:** inline, ink text, emphasis is the underline on hover, never a color.
- **Disabled:** `surface-2` fill, `mute` text, no shadow.

### Highlight Tag — the signature element
A tilted marker swipe, not a UI chip. Sentence case, 1 to 3 words, Noto Sans
extrabold, single line, `whitespace-nowrap`.
- **Fill:** a highlighter-cast 100 tint (yellow/lime/green/spring) or lavender/white; **ink text always**.
- **Shadow:** a hard `0 4px 0 0` offset in a *darker tone of the fill* (never black), plus a faint `0 6px 12px` ambient.
- **Tilt:** always clearly skewed — the scale is -6°/-4°/-3° (left) and 3°/4°/6° (right). There is **no 0° / flat option**; default is -4°.
- **Sizes:** md (14px radius, `text-lg`), lg (18px radius, `text-[28px]`), xl (`rounded-2xl`, `text-4xl`).
- **Placement:** only above a **left-aligned** title; on a centered header it is omitted entirely (enforced in `marketing/section-header.tsx`).

### Cards / Containers
- **Corners:** generous — `rounded-3xl` (28px) for content cards, up to `rounded-4xl` (32px) for header-pattern panels; `rounded-lg` (12px) for tight UI. Nested cards are forbidden.
- **Background:** `surface` (#ffffff) sitting one step above `paper`.
- **Border:** 1px `line`; this, not a shadow, defines the card at rest.
- **Hover:** a restrained lift — `translateY(-1.5)` + upgrade to `md`/`lg` shadow, 300ms `--ease-pm`. A whole clickable card may add an up-right arrow that nudges on hover.
- **Padding:** 28–32px (`p-7`/`p-8`).

### Meta pills & chips
Small `surface-2` fill, `pill` radius, ink-2 label, 1px border. Used for dates,
formats, counts. Categorical chips may take a highlighter-cast fill. Never colored text.

### Inputs / Fields
Surface fill, 1px `line` stroke, 12px-family radius. Focus shifts the border to
blue and adds the 3px `blue/20` ring (identity). Sentence-case labels and
placeholders.

### Navigation
Sticky top bar on paper with a hairline bottom rule. Ink links, sentence case,
weight for the active state, `surface-2` tint on hover — never a colored link.
Primary action is the orange **Join on #Slack**. Mobile collapses to a menu button.

### Signature set-pieces & motion
- **Master hero** — a blue *drenched* field: the 135° `blue-bright → blue → blue-press` gradient, floating orbs (`pm-float`), the script "Makers" watermark (see The Watermark Rule), and a workspace screenshot in a browser frame. The loudest surface in the system.
- **The Watermark Rule.** The "Makers" script appears in backgrounds at ONE treatment only, implemented once in `pm/script-watermark.tsx` — never hand-roll a second. The BLACK script, zoomed to 180% of the band's width and centered, so the letterforms bleed off every edge and the word never reads in full. Opacity is a whisper that darkens the ground tone-on-tone: 8% on blue set-pieces (reads as a deeper blue), 5% on light grounds (reads as a soft grey). No blur, no rotation beyond the script's natural slant, always `aria-hidden` and behind every content layer. The ground it sits on is always the brand wash: blue set-pieces run the 135° `blue-bright → blue → blue-press` gradient (plus at most a soft glow orb); light grounds stay paper with a gentle `blue-soft`/lavender wash.
- **The Washed Voices Band.** Every testimonial/quote carousel (`Marquee` of quote cards) sits on the same transition treatment, not a flat `paper`/`surface-2` band: a vertical wash that rises out of whatever surface precedes it, peaks at `blue-soft` behind the cards, and settles into whatever surface follows — `bg-linear-to-b from-{prev} via-pm-blue-soft/70 to-{next}` (a hero directly above hands off from full blue instead: `from-pm-blue-soft`). Layer in, in order: the light-tone `ScriptWatermark`, `GlowField`, then the content at `relative`. White quote cards pop off the wash; the `Marquee` edge-fade is a transparent mask so it never smears a wrong color. This is what turns a hero→content or content→content seam from an abrupt cut into a held note.
- **Page headers** — per-program blue bands with distinct backdrops (blueprint grid for Alt School, hexagon mesh for Mentoring, washed event photo for Jam) so pages don't read as one template.
- **Grow / Build / Connect** — the three-pillar spine and the *only* sanctioned icon set; icons are dropped where they'd repeat redundantly.
- **Motion primitives:** `Reveal` (fade + directional slide, optional blur-in, `700ms` `cubic-bezier(0.2,0,0,1)`), `Stagger` (cascades reveals ~90ms apart), `CountUp` (stats animate 0→value on scroll, `tabular-nums`), `Marquee` (seamless revolving strip, pause-on-hover, edge-fade), `Magnetic` (a CTA leans toward the cursor), `GlowField` (a soft `blue-glow/25` blur that drifts after the cursor inside a Washed Voices Band, eased with a lerp so it trails rather than sticks; rests centred on touch). Entrance uses `.pm-rise`. **Every one is reduced-motion safe** — content is forced visible and numbers jump to final; `GlowField` and pointer-follow effects are skipped outright under `(hover: none)` or reduced motion. Ease-out only, no bounce; layout properties are never animated.

## 6. Do's and Don'ts

### Do:
- **Do** paint with the two brand colors in role: blue `#3f3fff` for identity (logo, focus rings, hero field), orange `#ff5500` for the single action per screen.
- **Do** open a section with its title, or with a left-aligned skewed `HighlightTag`, and nothing above it.
- **Do** keep every `HighlightTag` clearly tilted (3° minimum) with a hard bottom shadow in a darker tone of its own fill.
- **Do** build structure with 1px `#dcdde1` rules and tonal steps (paper → surface → surface-2); reach for a shadow only on hover/float/focus.
- **Do** set everything in Noto Sans / Noto Sans Display, sentence case, hierarchy from weight + size.
- **Do** write welcoming, second-person, Slack-fluent copy; buttons are 1 to 3 word imperatives; make "free" the headline.
- **Do** show real faces, names and event photos; when a photo is missing use an initials avatar, never a fabricated person.
- **Do** let titles use the available width and only wrap when they truly must; give leads `max-w-4xl` when left-aligned.
- **Do** keep motion reduced-motion safe, eased-out, and off layout properties.

### Don't:
- **Don't** apply blue, orange, or any highlighter hue to *text* for emphasis or as a link color. No colored text, ever. (Link = weight + underline or arrow.)
- **Don't** put an eyebrow / kicker over a title — no small tracked uppercase label ("ABOUT US", "WHAT WE DO") sitting above a heading.
- **Don't** use a script or cursive font, or any face mimicking the "Makers" wordmark; the wordmark is an SVG image, never type.
- **Don't** fill a CTA with blue or use orange for anything but the one conversion button per screen.
- **Don't** stack a `Highlighter` marker-sweep and a `HighlightTag` on the same title, and don't center a tag.
- **Don't** use em dashes in copy — use commas, colons, periods, or parentheses. Also not `--`.
- **Don't** add decorative icons, step numbers, or random separators; only the Grow / Build / Connect set is sanctioned.
- **Don't** ship the SaaS-landing template: cream background, Inter, gradient-text hero, the big-number stat-row template, or identical icon-heading-text card grids. Vary rhythm and tie numbers to faces/context.
- **Don't** use glassmorphism, glow, neon-on-black, side-stripe (`border-left`) accents, gradients on chrome, or nested cards.
- **Don't** introduce dark mode or a purple/gradient AI-tool skin; if it could read "AI made that," rework it.
