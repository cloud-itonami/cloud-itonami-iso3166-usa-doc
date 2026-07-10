# Business Model: Independent Commerce/BIS Export-Control Compliance Service — United States

## Classification

- Repository: `cloud-itonami-iso3166-usa-doc`
- ISO 3166 (agency-level): `USA-DOC`, parent `USA`
- Ooyake cross-reference: `gov.usa.doc` (Department of Commerce)
- Activity: BIS EAR classification and export-license screening for public-sector delivery

## Customer

- an operator already using `cloud-itonami-iso3166-usa` whose contract
  touches Department of Commerce rules or buying channels
- a foreign SME entering a Department of Commerce-specific public program for the first time

## Offer

- walkthrough and evidence checklist for: BIS EAR classification and export-license screening for public-sector delivery
- ongoing regulatory-change monitoring for this body's public sources
- compliance-audit export package

## Trust Controls

- `:filing/submit` never auto-commits at any phase
- fabricated regulatory claims are HARD holds
- not legal advice — cite https://www.bis.doc.gov/

## Boundary

- **`cloud-itonami-iso3166-usa`**: country coordinator (general U.S. market entry)
- **`com-etzhayyim-ooyake`**: read-only civic atlas (never acts as the body)
