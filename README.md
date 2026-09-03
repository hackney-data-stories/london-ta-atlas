# London Temporary Accommodation Atlas

A borough-level map of temporary accommodation across all 33 London
boroughs, built entirely from public data.

**Live site:** (add the URL once connected)

## Deploying

Site files are in `public/`. Two Cloudflare routes both work:

- **Workers** (the current dashboard flow): `wrangler.jsonc` declares
  `public/` as static assets. Deploy command `npx wrangler deploy`,
  build command blank.
- **Pages** (legacy flow): framework preset None, build command blank,
  build output directory `public`.

There is no build step either way — the files are already the site.

## What it shows

Households in temporary accommodation and the mix of arrangements; how
long people stay and whether that is getting longer; children in
temporary accommodation; placements outside the borough; bed and
breakfast placements with children beyond the six-week legal limit; and
— where the published payment data supports it — what boroughs pay per
night.

Click any borough for the full picture.

## Sources

All Open Government Licence:

- MHCLG, Statutory homelessness in England, detailed local authority tables, quarters to 31 March 2026 (TA1, TA4, TA4c, TA7, TA8, TA9)
- The 33 boroughs' published payments over £500
- ONS Open Geography Portal, Local Authority Districts Dec 2024
- Access provider site and Find a Tender notices (ADAM adoption)

## What this map deliberately does not do

- **It does not rank boroughs on spend.** Each borough's published
  payment file captures a different and unknowable share of its true
  bill — cost per household per night ranges from £3 to £107 across
  London, which measures publication practice rather than procurement.
- **It does not compare an operator's price between boroughs** unless
  both payments sit under the same homelessness label. Ungated, the same
  firm's payments mix homelessness lets with children's semi-independent
  placements and Section 17 bed and breakfast — different products at
  different prices.
- **It does not show a rate where a borough batches its invoices.** A
  payment covering several units cannot be divided into a nightly rate,
  even when it happens to decode to a round number.

## Confidence

Household counts, length of stay, children and out-of-area placements
are MHCLG statutory returns — measured. Nightly rates are *decoded* from
councils' own published payment files and remain inference until an
officer confirms one against an invoice. One external check exists: a
decoded £87.84 a night for Havering against that council's own published
average of £88.29.

MHCLG figures are a snapshot on the last day of each quarter, so length
of stay is time served to date by households still present, not
completed duration.

## Corrections

If you are an officer or member in one of these boroughs and a figure
looks wrong, please open an issue. Several figures here were wrong at
some point and were corrected; that is expected, and being told is the
fastest route to accuracy.

---

Built from analysis at commit `{rev}`. Data regenerated quarterly when
MHCLG publishes.
