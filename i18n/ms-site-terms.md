# Site term sheet - Bahasa Melayu (Malaysia)

Scope: buildwithjesus.com (site copy, not the guide). Pilot: homepage live 8 Oct 2026.
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
- Nav links point at English pages until each page is translated.

## Status

Homepage live (commit pending). Next: agent page, then leaders/workshop/groups.
