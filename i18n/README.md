# Build with Jesus site - translation programme

The website is translated the same way as the one to eight guide: **root English plus
`/<lang>/` directories**. Languages start with Bahasa Melayu (`/ms`) and Tagalog (`/tl`).

## How it works

- `_loc_build.py` in the site root builds `ms/index.html` and `tl/index.html` from
  `index.html`. It strips the EN language switcher back to baseline first, then applies
  count-asserted structural edits, attribute edits, masked-block edits (JSON-LD, JS, CSS),
  and an exact-string text map. Gates: tag-stream equality, size ratio, no em/en dashes,
  banned-word sweep, required-term sweep, English-leftover probe.
- `_loc_en_switcher.py` keeps the EN page in sync (switcher chips, mobile menu language
  group, hreflang cluster) and maintains `sitemap.xml` and `llms.txt`.
- Every page carries the reciprocal hreflang cluster: en, ms, tl, x-default.
- Term sheets per language live beside this file. Change a term in one language's sheet
  and rebuild that language; never hand-edit a built page.

## Status

- Homepages: EN, `/ms`, `/tl` live (8 October 2026). Switcher on all three homepages.
- Remaining pages (agent, leaders, workshop, groups, examples, inspiration, ai, safety,
  legal): English only, to follow language by language.
- Nav links on translated homepages point at the English pages until each page is
  translated; a later pass routes them per locale.

## Rules carried over from the guide

- No em dashes or en dashes in translated prose; no local "teen" words (ms: never
  "remaja"; tl: never "tinedyer").
- Numbers stay Western digits; HTML entities stay entities; brand names (Build with
  Jesus, one to eight, onetoeight) stay English.
- Scripture: where a language pack exists (tl: tglulb) quote exactly from the shipped
  file and name the translation; where none exists (ms, pending a verified source)
  quote the English exactly with WEB named and keep the reference's book name in the
  reader's language.
