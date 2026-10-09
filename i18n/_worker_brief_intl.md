# Worker brief: translate one buildwithjesus.com page (international languages)

You are translating exactly ONE page of buildwithjesus.com into ONE language
(id, vi, th, es, zh, ko or ja). Your entire deliverable is one JSON file.

## What you produce

`C:/Users/insig/projects/buildwithjesus/i18n/_maps/<lang>/<page>.json`:

```json
{
  "runs": { "<exact English text>": "<translation>", "...": "..." },
  "attrs": { "<exact English attribute value>": "<translation>", "...": "..." },
  "notes": "anything I should know (optional)"
}
```

- `runs` translate the visible text of the page.
- `attrs` translate attribute values (alt text, aria-labels, meta descriptions, titles).
- The shared navigation and footer are already translated in `i18n/_shared_<lang>.json`
  for your language; the checker subtracts those automatically. Do NOT duplicate them.
- Scripture blocks (passages, the Lord's Prayer, the Ten Commandments, citation lines)
  are handled by dedicated scripture machinery. They are masked out of the run list.
  Do not include them anywhere.
- The Ten Commandments grid on the AI page stays English on every language by design.
  Do not translate it.

## Your loop (follow exactly)

1. Read the English page `C:/Users/insig/projects/buildwithjesus/<page>.html` (read it all).
2. Read your site term sheet: `C:/Users/insig/projects/buildwithjesus/i18n/<lang>-site-terms.md`
   (LOCKED terms, register, banned words; it wins over your own instincts).
3. See exactly what is missing: run
   `"/c/Users/insig/AppData/Local/hermes/hermes-agent/venv/Scripts/python.exe" -u _loc_map_check.py <page> <lang>`
   in `C:/Users/insig/projects/buildwithjesus`. It lists every run and attr that needs
   a translation (and flags banned words, dashes, entities).
4. Write the JSON file with every missing key translated.
5. Run the checker again until it says PASS.
6. Reply with a 2-3 line summary + anything in `notes`.

## Rules that matter (hard)

- **Natural language, not word-for-word.** No machine-translation stiffness.
- Keys must be copied EXACTLY (including HTML entities like `&amp;` `&middot;` `&#8594;`
  `&#8217;`). Values keep entities as entities; NEVER raw curly quotes; a bare `&` must
  not appear (use `&amp;`).
- **No em dashes or en dashes** (no `—` `–` `&#8211;` `&#8212;`); use comma, colon or stop.
- **Prices/amounts stay verbatim**: `$19.99 (AUD)`, `$29.99 (AUD)`, `$69.99 (AUD)`,
  `$1,000 (AUD)`, `$20`. Dates follow your term sheet.
- **Brand tokens stay English**: `Build with Jesus`, `one to eight`, `onetoeight`,
  `OpenRouter`, `Telegram`, `WhatsApp`, `AI`. The agent word and Bible word follow your
  term sheet exactly.
- **No teen-framing words.** Your term sheet lists them; the checker fails any hit.
- Every value must differ from its English key (except licensed loanwords like `Agent`,
  `Workshop` where the term sheet says the loan stays).
- Write ONE file. Do not touch any other file. UTF-8 JSON.
