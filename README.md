# Claire Cahill Art: Shopify theme

Horizon 3.5.1 with a small gallery layer on top. Stock Horizon files are untouched except
`layout/theme.liquid` (adds a `template-*` body class) and `snippets/stylesheets.liquid`
(loads `assets/cc-gallery.css`).

## Branches

- `main`: the live theme exactly as exported from clairecahillart.com on 29 Oct 2026.
- `redesign`: the new gallery design. Connect this branch in Shopify as an unpublished theme.

## What's custom

| File | Used on | What it does |
|---|---|---|
| `sections/cc-hero.liquid` | Home | Artist name, intro, one artwork with an optional wall-label caption |
| `sections/cc-rooms.liquid` | Home | One tile per gallery room, read from the main menu |
| `sections/cc-works.liquid` | Home | Grid of pieces from any collection |
| `sections/cc-feature.liquid` | Home, About | Image with story; also works text-only |
| `sections/cc-techniques.liquid` | About | Techniques with close-up images |
| `sections/cc-quote.liquid` | Any page | Pull quote |
| `sections/cc-contact.liquid` | Contact | Contact form with topic menu |
| `sections/cc-collection-header.liquid` | Gallery and rooms | Title, intro and room links |
| `snippets/cc-piece.liquid` | Everywhere | Matted image plus wall label (title, type or "Original", price) |
| `assets/cc-gallery.css` | Everywhere | Tokens and shared styles |

## How rooms work

Rooms are automated collections, one per product tag. The homepage tiles and the gallery's
room links both read the collections in the **main menu**, including any nested under a
"Gallery" dropdown. To add a room (florals, line drawings, collage):

1. Products > Collections > Create collection, set to Automated, condition
   **Product tag is equal to** the new tag, for example `florals`.
2. Online Store > Navigation > Main menu: add the collection under Gallery.

It then appears in the header dropdown, on the homepage and on the gallery page. No code.

Tags are case-sensitive. Keep new tags lowercase.

## Wall labels

A product tagged `original` shows "Original, one of a kind" under its title. Every other
product shows its Product type (Print, Mug, Blanket...), so set the type in Printify or admin.
