# Guida di avvio — Open Geomatics Education

Procedura per mettere online il progetto. Tempo stimato: **circa 1 ora**, una sola volta.
Tutto è gratuito. Sostituite ovunque `OpenGeomaticsEducation-PoliTO` con il nome scelto dal gruppo.

---

## Fase 0 — Decisioni preliminari (riunione di gruppo)

- [ ] **Nome del gruppo** e nome dell'Organization GitHub (deve essere libero: verificate su `github.com/<nome>`).
- [ ] **Maintainer iniziali**: almeno 3, possibilmente di atenei diversi.
- [ ] **Casella email di gruppo** (es. Gmail gratuita) per l'account Zenodo custode e per il Code of Conduct.
- [ ] Verifica del **regolamento di ateneo** sui materiali didattici e la licenza CC BY.
- [ ] Logo semplice (anche solo tipografico).

## Fase 1 — GitHub Organization (10 min)

1. Con il vostro account personale: **github.com → + → New organization → Free**.
2. Nome: `OpenGeomaticsEducation-PoliTO`. Email di contatto: la casella di gruppo.
3. **People → Invite member**: invitate gli altri maintainer con ruolo **Owner**.
4. **Settings → Member privileges**: Base permission = *Read*.
5. Create un **Team** `members` con permesso *Write* sul repository.
6. **Settings → Authentication security**: richiedete la 2FA a tutti i membri.

## Fase 2 — Repository e sito (15 min)

1. Nell'Organization: **New repository** con nome esatto `OpenGeomaticsEducation-PoliTO.github.io`, *Public*.
2. Caricate il contenuto di questa cartella (**Add file → Upload files**, trascinando tutto, oppure con `git push`).
   - Nota: le cartelle che iniziano con il punto (`.github`, `.zenodo.json`) a volte non vengono trascinate dal browser; in quel caso usate GitHub Desktop o `git`.
3. **Settings → Pages → Source: GitHub Actions**.
4. Al primo commit parte la pubblicazione automatica (scheda **Actions**, circa 2–3 min).
5. Il sito sarà su `https://OpenGeomaticsEducation-PoliTO.github.io`.
6. **Settings → General → Topics**: aggiungete `geomatics, geodesy, surveying, oer, open-educational-resources, gnss, photogrammetry`.
7. **Settings → Branches → Add rule** su `main`: *Require a pull request* con *1 approval*. Questo applica la regola di revisione del GOVERNANCE.

## Fase 3 — Zenodo (20 min)

1. Create l'**account custode** su zenodo.org con la casella di gruppo, con accesso email + password (le Organization GitHub non possono fare login su Zenodo). Conservate la password nel password manager condiviso tra maintainer.
2. **Communities → New community**: identificativo `opengeomaticseducation`, aggiungete gli altri maintainer come *Curator* o *Owner*.
3. Dall'account custode: **Profilo → GitHub → Sync** e attivate il toggle sul repository.
   - Serve che l'account GitHub collegato abbia accesso all'Organization. Opzione semplice: collegate l'account GitHub di un maintainer, poi condividete ogni record creato con l'account custode e gli altri maintainer (**Record → Share → Manage**).
4. Su GitHub: **Releases → Draft a new release → tag `v1.0.0`** → Publish.
5. Zenodo crea il record usando `.zenodo.json`: il **gruppo compare come primo creator**, seguito dagli autori con ORCID.
6. Copiate il **DOI concettuale** (quello che resta valido per tutte le versioni) in `about.qmd`, `README.md` e `CITATION.cff`.

**DOI per singola risorsa matura:** Zenodo → New upload → tipo *Lesson*; caricate lo `.zip` della risorsa; creator: gruppo + autori; Community: la vostra; *Related identifier*: URL della pagina live. Poi inserite il DOI nel campo `doi:` del suo `index.qmd`.

## Fase 4 — Scopribilità (20 min)

- [ ] **Google Search Console** (gratuito): aggiungete la proprietà `https://OpenGeomaticsEducation-PoliTO.github.io` (verifica tramite file HTML caricato nel repo) e inviate `sitemap.xml`, generata da Quarto.
- [ ] **OER Commons**: account gratuito → *Add OER* → inserite URL e metadati delle risorse principali; create un *Group* con il nome del gruppo.
- [ ] **MERLOT**: registrazione gratuita come *member* → *Contribute material*.
- [ ] **OERSI**: indicizza automaticamente i record Zenodo con tipo *Lesson* o *Educational material* e licenza aperta; verificate dopo qualche settimana che compaiano su oersi.org.
- [ ] **ORCID**: ciascun autore importa i record Zenodo nel proprio profilo (ORCID → Works → Add → Search & link → DataCite).
- [ ] Annuncio nelle reti di riferimento: working group ISPRS/IAG, mailing list, social e newsletter di dipartimento.

## Fase 5 — Lavoro ordinario

| Azione | Come |
|---|---|
| Correggere un refuso | Sito → *Edit this page* → modifica nel browser → *Propose changes* |
| Nuova risorsa | Copia `resources/_template/`, compila, Pull Request |
| Revisione | Un altro membro approva la Pull Request → pubblicazione automatica |
| Nuova versione citabile | GitHub → *Releases* → nuovo tag (es. `v1.1.0`) → Zenodo aggiorna il DOI |

## Cosa personalizzare subito

1. Nome del gruppo in: `_quarto.yml`, `index.qmd`, `about.qmd`, `README.md`, `CITATION.cff`, `.zenodo.json`, footer dei worksheet.
2. **ORCID reali** (ora ci sono segnaposto `0000-0000-0000-0000`).
3. Elenco membri in `about.qmd`.
4. Email di contatto in `CODE_OF_CONDUCT.md`.

## Per lavorare in locale (facoltativo)

Installate [Quarto](https://quarto.org/docs/get-started/) e, dalla cartella del progetto, lanciate `quarto preview`: il sito si apre nel browser e si aggiorna a ogni modifica.
