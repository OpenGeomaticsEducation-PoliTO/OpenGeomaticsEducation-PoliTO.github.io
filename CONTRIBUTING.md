# Contributing

Thank you for helping improve open geomatics education!

## Quick contributions (no installation)

- **Report an error:** open an issue with the *Report an error* form.
- **Fix a typo:** click *Edit this page* on the website, edit in the browser, click *Propose changes*.

## Adding a new resource

1. Copy `resources/_template/` to `resources/<short-name>/` (lowercase, hyphens).
2. Fill in **all** metadata fields at the top of `index.qmd`, including the JSON-LD block (it makes the resource findable by search engines).
3. Write the learning objectives, background, activity and instructor notes.
4. Add the interactive part as `worksheet.html`.
5. Remove `draft: true` and open a pull request.

## Quality checklist (checked by the reviewer)

- [ ] Title, description and keywords in English
- [ ] Level, duration, prerequisites, learning objectives filled in
- [ ] Authors with ORCID and affiliation; CRediT roles
- [ ] `worksheet.html` is **self-contained**: no external CDNs, fonts or trackers; works offline
- [ ] Works on a phone-sized screen
- [ ] No third-party material without a compatible licence (CC BY, CC0, public domain) and attribution
- [ ] Formulas and numerical results verified
- [ ] Footer with credits, licence and "Report an error" link

## Style

- English as primary language; translations in a subfolder `it/`, `es/`, … with the same structure.
- Clear, short sentences; define symbols when introduced.
- Prefer SI units and explicit angular units (°, gon, rad, ″).

## Credits

Every contributor is credited. Authors appear on the resource; reviewers and editors in the `reviewers` field and in the Zenodo record.

By contributing you agree that your contribution is released under CC BY 4.0 (content) and MIT (code),
and you follow our [Code of Conduct](CODE_OF_CONDUCT.md).
