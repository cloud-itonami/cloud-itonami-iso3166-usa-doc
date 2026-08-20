# cloud-itonami-iso3166-usa-doc

Open ISO 3166 **agency-level** Blueprint for **USA-DOC**: Department of Commerce
(parent country: **USA**).

This leaf designs a forkable OSS business for an independent operator
navigating **Department of Commerce**-specific regulatory compliance —
especially **BIS EAR** classification and export-license screening —
composing with the country coordinator `cloud-itonami-iso3166-usa`.

## What this is NOT

- **Not the Department of Commerce.** Commercial compliance navigation only.
- **Not legal advice.** Cite official sources; route licensed work to counsel.
- **Not ITAR and not FAR.** The EAR (15 CFR chapter VII subchapter C, BIS) is
  a different book from the ITAR (22 CFR subchapter M, State/DDTC) and from
  federal acquisition (48 CFR). The catalog below exists to keep those three
  from collapsing into one “Commerce paperwork” story.

## The verified catalog

`src/statute/facts.cljc` is the spec-basis: **39 regulatory anchors across three
CFR titles (15, 22, 48), 16 byte-exact quotes of live regulation text, and 4
checked absences.** Every heading is the byte-exact `label_description`
returned by the official eCFR versioner API, and every quote is a byte-exact
span of the section text returned by the same API, both pinned to the
`2026-08-18` snapshot.

```bash
nbb tools/verify_citations.cljs     # live gate: re-fetches eCFR, exits 0/1/2
clojure -M:test                     # offline invariants
clojure -M:lint
```

| exit | meaning |
|---|---|
| 0 | answered; every heading, quote and absence checked out, floors met |
| 1 | answered; something drifted — the message names which entry |
| 2 | **could not answer** — network, undeclared endpoint, broken control, or below floor |

Top-level `:deps` is empty on purpose (ADR-2608201300): the catalog is plain
data; lint/test tool coords stay under aliases only.

## Official surface

- https://www.commerce.gov/
- https://www.bis.doc.gov/

## Capability layer

Resolves via `kotoba-lang/iso3166` (`USA-DOC`, parent `USA`).

## License

AGPL-3.0-or-later.
