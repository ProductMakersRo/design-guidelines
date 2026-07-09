# Product Makers — design guidelines

The brand and design system for [Product Makers Romania](https://www.productmakers.ro),
extracted from the community website. Two files, one source of truth:

- **[DESIGN.md](DESIGN.md)** — the human- and AI-readable brief. Colours, type,
  elevation, components, and the do's and don'ts, in the
  [Stitch DESIGN.md format](https://stitch.withgoogle.com/docs/design-md/format/)
  (YAML token frontmatter plus six fixed sections). Hand it to a designer, or
  paste it into an AI, to produce visuals that read as Product Makers.
- **[design.json](design.json)** — the machine-readable companion. What the
  frontmatter can't hold: 8-step tonal ramps per colour, shadow and motion
  tokens, self-contained component snippets, and the full narrative. Inside an
  app this file lives at `.impeccable/design.json`.

## The system in one line

A well-typeset makers' zine: black display type on warm paper, two loud paint
colours (blue `#3f3fff` is identity, orange `#ff5500` is action), and the
signature tilted highlighter-marker labels. Structure comes from 1px rules, not
shadows. It should feel made by a person, not generated.

## Using it

Read `DESIGN.md` top to bottom before making anything. The Named Rules and the
Do's and Don'ts are non-negotiable; they are what keep new work on-brand. When
the system changes, update `DESIGN.md` first, then regenerate `design.json` so
the two never drift.
