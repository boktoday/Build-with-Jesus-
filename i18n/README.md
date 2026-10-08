# Build with Jesus site - translation programme

The website is translated the same way as the one to eight guide: **root English plus
`/<lang>/` directories**. Languages start with Bahasa Melayu (`/ms`) and Tagalog (`/tl`).

## How it works

- `_loc_build.py` builds the two homepages from `index.html`; `_loc_pages.py` builds the
  nine sub-pages via `_loc_common.py`. Both follow the same discipline: strip the EN
  switcher back to baseline, count-asserted structural edits, masked-block edits
  (JSON-LD/JS/CSS, and on inspiration/ai the scripture and governing-document regions),
  attribute edits, then an exact-string text map walk. Gates: unmapped runs abort, size
  ratio band, dash sweep, banned-word sweep, required-term sweep (word-boundary aware),
  English-leftover probes, bare-internal-href check.
- `_loc_en_all.py` / `_loc_en_switcher.py` keep every EN page in sync (switcher chips,
  mobile menu language group, hreflang cluster); `_loc_sitemap.py` maintains `sitemap.xml`
  and `llms.txt`. `_loc_index_navfix.py` points the locale homepages' nav links inside the
  locale. `_loc_qc_all.py` renders all 20 pages locally with content/link/image checks.
- Per-page translation maps live in `i18n/_maps/<lang>/<page>.json` (runs + attrs); shared
  chrome in `i18n/_shared_<lang>.json` always wins. `_loc_map_check.py <page> <lang>` is
  the validator workers iterate on.
- Every page carries the reciprocal hreflang cluster: en, ms, tl, x-default.
- Term sheets per language live beside this file. Change a term and rebuild; never
  hand-edit a built page.

## Status

- Full site live in EN, /ms and /tl (8 October 2026): homepage plus agent, leaders,
  workshop, groups, examples, inspiration, ai, safety, legal.
- Nav links stay inside each locale; switcher and hreflang on every page; sitemap carries
  all 20 URLs.
- Follow-ups: one native review pass per language (term sheets are the working base);
  Malay awaits a verified Bible edition. tglulb carries a typo in one commandment verse
  ("manirahanng"), kept exact per the quoting rule; flag upstream at review.

## Rules carried over from the guide

- No em dashes or en dashes in translated prose; no local "teen" words (ms: never
  "remaja"; tl: never "tinedyer").
- Numbers stay Western digits; HTML entities stay entities; brand names (Build with
  Jesus, one to eight, onetoeight) stay English.
- Scripture: where a language pack exists (tl: tglulb) quote exactly from the shipped
  file and name the translation; where none exists (ms, pending a verified source)
  quote the English exactly with WEB named. Tagalog swaps live in
  `i18n/tl-scripture-swaps.json` (39 exact swaps on the inspiration page); the KJV
  prayer block stays KJV (it carries its own audio). The ai page's Ten Commandments grid
  is a governing document: kept English on both locales, flagged in page copy.
