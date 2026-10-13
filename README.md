# Open Geomatics Education

**Free, open educational resources in geomatics, geodesy and surveying** — exercises, lecture notes and interactive HTML worksheets, ready to use in class or for self-study.

🌐 **Website:** https://OpenGeomaticsEducation-PoliTO.github.io
📦 **Archive & DOI:** https://zenodo.org/communities/opengeomaticseducation
📜 **Licence:** content [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · code MIT

## What you find here

| Resource | Level | Topics |
|---|---|---|
| [Repeated Angle Measurements](resources/repeated-angle-measurements/) | Bachelor | surveying, measurement theory |
| [Photogrammetric Flight Planning](resources/photogrammetric-flight-planning/) | Bachelor / Master | photogrammetry, flight planning, UAV |

All worksheets run in the browser, need no installation and work offline.

## Repository structure

```
_quarto.yml            site configuration
index.qmd              home page with resource catalogue
about.qmd              members, credits, how to cite
contribute.qmd         how to contribute
resources/
  _template/           copy this to create a new resource
  <resource-name>/
    index.qmd          resource card (metadata, objectives, instructor notes)
    worksheet.html     self-contained interactive worksheet
CITATION.cff           citation metadata (GitHub + Zenodo)
.zenodo.json           Zenodo deposit metadata (group as creator)
GOVERNANCE.md · CONTRIBUTING.md · CODE_OF_CONDUCT.md
.github/workflows/     automatic publishing to GitHub Pages
```

## How to cite

See [CITATION.cff](CITATION.cff) or the "Cite this repository" button on GitHub.

## Contribute

Teachers, researchers and students are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

---
*Open Geomatics Education Group — topics: geomatics, geodesy, surveying, gnss, photogrammetry, least-squares, oer, open-educational-resources*
