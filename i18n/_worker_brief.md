# Worker brief: translate one buildwithjesus.com page

You are translating exactly ONE page of buildwithjesus.com into ONE language (Bahasa Melayu `ms` or Tagalog `tl`). Your entire deliverable is one JSON file. You do not touch any other file.

## What you produce

`C:/Users/insig/projects/buildwithjesus/i18n/_maps/<lang>/<page>.json` with this shape:

```json
{
  "runs": { "<exact English text>": "<translation>", "...": "..." },
  "attrs": { "<exact English attribute value>": "<translation>", "...": "..." },
  "notes": "anything I should know (optional)"
}
```

- `runs` translate the visible text of the page.
- `attrs` translate attribute values (alt text, aria-labels, meta descriptions, og/twitter titles and descriptions).
- The site's shared navigation and footer are already translated in `i18n/_shared_<lang>.json`; the checker subtracts those automatically. If you think a shared rendering is wrong FOR THIS PAGE, note it in `notes`; do not duplicate-shift it.

## The loop (follow exactly)

1. Read the English page: `C:/Users/insig/projects/buildwithjesus/<page>.html` (read it all, so translations fit the page's story).
2. Read the term sheets for your language:
   - `C:/Users/insig/projects/buildwithjesus/i18n/ms-site-terms.md` or `tl-site-terms.md`
   - The guide glossaries (locked names): `C:/Users/insig/AppData/Local/hermes/skills/productivity/html-content-translation/references/onetoeight-ms-glossary.md` and `.../onetoeight-tl-glossary.md`
3. Run the checker from the repo root:
   `"/c/Users/insig/AppData/Local/hermes/hermes-agent/venv/Scripts/python.exe" _loc_map_check.py <page> <lang>`
   It prints every MISSING run and attribute, verbatim, one per line. Those exact strings are your translation keys.
4. Write (or edit) your JSON file with a key for every missing item and your translation as the value. Copy each English key EXACTLY as printed - character for character, including `&amp;`, `&#8217;`, `&middot;` entities and the trailing punctuation. Do not retype from the page; paste from the checker output.
5. Run the checker again. Fix what it flags (missing items, extra keys that are not on the page, banned words, dashes). Repeat until it prints `RESULT: PASS`.

## Rules for the translation values

- Audience and voice: warm, plain, direct, respectful. The site speaks to young people (13-23) and the adults who lead them. Never use the local term for "teen(s)".
- Locked terms:
  - ms: young people = **orang muda** (never "remaja"); adults = **orang dewasa**; church = **gereja**; the Bible = **Alkitab**; the agent = **agent** (loanword, never "ejen"); leaders guide = **panduan pemimpin**; workshop = **bengkel**; the guide = **panduan**; programme = **program**; build day = **hari bina**. Address the reader as **anda** (never "kamu"/"kalian"). Standard Malaysian spelling and months (Disember, Ogos, Mac, Jun, Julai). Avoid Indonesian forms entirely: bisa (use boleh), karena (kerana), kantor (pejabat), layar (skrin), menit (minit), konten (kandungan), kalian (anda semua), Desember/Agustus/Maret (Disember/Ogos/Mac), banget/udah/nggak (very informal Indonesian - never).
  - tl: young people = **kabataan** (never "tinedyer" or "teenager"); adults = **matatanda**; church = **simbahan**; the Bible = **Bibliya**; the agent = **agent**; leaders guide = **gabay ng mga lider**; the guide = **ang gabay**; workshop = **workshop** (or "pagsasanay" where natural); build day = **araw ng paggawa**. Address the reader as **ka / ikaw / mo** (never "po", never "kayo"/"ninyo"). Natural Filipino, not stiff textbook Tagalog.
- Punctuation: NEVER use em dashes or en dashes. Use a hyphen, a comma, or rephrase.
- Quotes in values: use plain ASCII `'` for apostrophes or the entities `&#8216; &#8217; &#8220; &#8221;` for typographic quotes. Do not type raw curly quote characters. Write `&amp;` for ampersands. If the English key contains `&middot;`, keep `&middot;` in the value.
- Keep EXACTLY, untranslated, inside values:
  - `Build with Jesus`, `one to eight`, `onetoeight`, `BUILD WITH JESUS`
  - `OpenRouter`, `Telegram`, `WhatsApp`, `wifi`, `YouTube`
  - Prices as written, e.g. `$29.99 (AUD)`, and `$20`
  - Numbers, dates, code, URLs, emails, `buildwithjesus.com`
  - `World English Bible` and `King James Version` wherever they appear (e.g. in captions), and any Bible book names inside such captions stay as written in English ON malay; on TAGALOG keep them as the key writes them too (scripture itself is handled separately; you never translate a Bible verse).
- The word "| Build with Jesus" at the end of titles stays `| Build with Jesus`.
- Fragments: some runs are sentence pieces that flow around links (e.g. "workshop page" in "Register your interest on the workshop page and we will..."). Translate them as the fragment that reads naturally in the assembled sentence.
- Headings and button labels: short, natural, no title-case calques. Sentence case.

## Page-specific notes

- `inspiration`: the page's Bible text, citations and verse references are handled by a separate scripture pipeline and are NOT shown to you - ignore anything you cannot find. The caption runs you WILL see mention `World English Bible` / `King James Version`: keep those names exactly, translate only the surrounding words. Do not translate the quoted YouTube video title.
- `ai`: the ten numbered items inside the big "Ten Commandments for AI Agents" box are a governing document and stay in English; they are not shown to you. Translate everything else.
- `legal`: keep the legal entity name `AI Orchestrator`, the ABN, the phone number, the email address and `Victorian`/`Victoria, Australia` place names as written; translate the surrounding sentences.
- `agent`, `leaders`, `workshop`, `groups`, `examples`, `safety`: ordinary prose pages; translate everything shown.

## Hard constraints

- Write ONLY your own JSON file under `i18n/_maps/`. Never edit HTML, scripts, term sheets, or another worker's file.
- Your final message: report the page, language, number of runs and attrs translated, any notes, and confirm the checker prints PASS.
