# Site term sheet - Bahasa Melayu (Malaysia)

Scope: buildwithjesus.com (site copy, not the guide). Full site live 8 Oct 2026.
Base: the guide's Malay term sheet (same voice and watchlist) extended with site terms.

## Voice

- `anda` for the reader, warm, plain, DBP standard, short sentences.
- No em dashes or en dashes; use commas, colons, full stops.
- Western digits; entities stay entities; `&middot;` kept for list dots.
- Indonesian-drift watchlist applies in full (bisa→boleh, layar→skrin, kantor→pejabat,
  menit→minit, konten→kandungan, kalian→anda semua, dates: Disember/Ogos/Mac/Jun/Julai).
  Enforced by the build script's banned-word gate.

## Term locks (site)

- young people -> orang muda (never "remaja"); adults -> orang dewasa
- youth group -> kumpulan orang muda; churches -> gereja; charities -> badan amal;
  religious schools -> sekolah agama; homeschool families -> keluarga homeschool
- agent -> agent (loanword, per the guide editions; NOT "ejen"); the agent (nav) -> Agent
- the Bible -> Alkitab (not "Bible"); translation names in citations (World English
  Bible, King James Version) stay English; scripture stays English with WEB named until
  a verified Malay edition can be quoted
- leaders guide -> panduan pemimpin; workshop -> bengkel; programme -> program
- the guide -> panduan; The Guide (footer) -> Panduan
- build (verb) -> bina / membina; build (result, noun) -> binaan; build day -> hari bina
- the Eight Essentials -> Lapan Esensial; the eight essentials (prose) -> lapan esensial
- the eight locked names: Kemampuan untuk duduk dalam kesunyian / Badan anda ialah rumah /
  Kemahiran yang berguna dalam dunia sebenar / Pertahanan diri digital / Komuniti yang
  nyata / Pengetahuan tanpa Wi-Fi / Preskripsi alam / Keyakinan yang teruji
- Follow Jesus -> Ikut Yesus; Give them away -> Berikan semuanya
- Learn. Build. Give. -> Belajar. Bina. Beri.
- school term -> penggal; machine -> mesin; laptop -> komputer riba; admin access ->
  akses pentadbir; notification -> notifikasi; message -> mesej; screen -> skrin

## Scripture policy on translated pages

No verified Malay edition ships yet (editions.json: "Malay and Thai await a verified
source"). So the homepage quotes stay ENGLISH exactly as shipped, with the reference's
book name in Malay and the translation named: "Mazmur 90:17 (WEB)", "Kolose 3:23 (WEB)".
When a verified Malay edition lands, swap these to quote it exactly and name it.

## Meta

- URL: buildwithjesus.com/ms; lang="ms-MY"; og:locale ms_MY; canonical /ms.
- Hero video is English (no Malay video yet).
- Nav links stay inside each locale; switcher and hreflang on every page.

## Status

- Full site live in Bahasa Melayu: homepage + agent, leaders, workshop, groups, examples,
  inspiration, ai, safety, legal (8 Oct 2026).
- Scripture on the inspiration page stays English with World English Bible named and a
  Malay note saying why; swap to a verified edition when it lands.

## Prices and dates (founding price, from 8 Oct 2026)

- "Founding price" = **Harga pengasas** (introduced for the $19.99 launch window).
- Amounts keep the English shape with (AUD): "$19.99 (AUD)", "$29.99 (AUD)", "$1,000 (AUD)".
  "$19.99 (AUD)" and "$29.99 (AUD)" are both on the machinery keep list, so bare price
  runs stay identical across locales by design.
- Dates: "1 Disember 2026"; "sehingga 1 Disember 2026" = until; "kemudian $29.99 (AUD)" = then.
  Sentence-start form: "Harga pengasas $19.99 (AUD) sehingga 1 Disember 2026, kemudian
  $29.99 (AUD)."; mid-sentence: "sebagai harga pengasas sehingga 1 Disember 2026, kemudian $29.99 (AUD)".
- Run shapes on file: agent card "Harga pengasas $19.99 (AUD) sehingga 1 Disember 2026,
  kemudian $29.99 (AUD). Sekali bayaran, tiada pembaharuan."; leader/agent note prefix
  "Harga pengasas sehingga 1 Disember 2026, kemudian $29.99 (AUD). ..." (after the ". &middot; "
  separator on the leaders page).
- When the window closes (1 December 2026), the reverse sweep is: drop "founding" phrasing,
  set every "$19.99 (AUD)" to "$29.99 (AUD)", and remove the machinery keep entry for
  "$19.99 (AUD)" only after no page carries it.
- **Leaders guide (changed same day):** no longer part of the founding window. It is
  **coming soon at $69.99 (AUD)** ("akan datang" in ms; pre-launch, drafting not started).
  The leaders page carries an "Inside the guide" section, six cards: week by week, six build
  playbooks, the quick start, the printable kit, leading the reading, updates forever
  (ms heading "Di dalam panduan"). "$69.99 (AUD)" is on the machinery keep list.
