# London Temporary Accommodation Atlas

A borough-level map of temporary accommodation across all 33 London
boroughs, built entirely from public data.

**Live site:** (add the Pages URL once connected)

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

## Licence and attribution

**Code:** MIT — see `LICENSE`. Reuse it, fork it, adapt it for your own
authority.

**Data:** Open Government Licence v3.0, and it stays that way. If you
reuse `public/ta_map.json` or `public/london_boroughs.geojson`, carry
these:

> Contains public sector information licensed under the Open Government
> Licence v3.0.
>
> Source: Office for National Statistics licensed under the Open
> Government Licence v.3.0.
>
> Contains OS data © Crown copyright and database right 2026.

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
