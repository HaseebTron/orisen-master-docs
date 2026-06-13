# Radar Sleep-Stage Literature - v2 Source-Access Chase

Status: Raw working research artifact
Authority level: Radar/ML raw research archive
Date created: 2026-06-13
Governing docs:
- `radar-ml/radar-sleep-stage-literature/literature-review-workflow.md`
- `radar-ml/radar-ml-read-rules.md`
- `ai-context/source-of-truth-rules.md`
- `ai-context/ai-operating-mode.md`
Source inputs:
- `radar-ml/radar-sleep-stage-literature/raw/v2-candidate-register-2026-06-13.md`

## Purpose

This artifact records legal source-access status for selected P0 hold sources only.

It is not extraction, synthesis, Orisen product evidence, Orisen product-claim support, or an interpretation of what these papers imply for Orisen.

## Scope

Source-access chase target IDs:

- RSL-001
- RSL-004
- RSL-006
- RSL-011
- RSL-013

## Access-status summary

| ID | Canonical title | DOI/stable ID | Sources checked | Best legal source found | PDF/full-text status | Version/fallback status | Extraction readiness after chase | Notes |
|---|---|---|---|---|---|---|---|---|
| RSL-001 | Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar | 10.1109/JBHI.2021.3072644; PMID:33848253 | DOI redirect, IEEE Xplore, PubMed, OpenAlex, Crossref, Europe PMC, arXiv exact-title check, normal web queries for title/PDF/author/institutional copy, Semantic Scholar API attempted but rate-limited | Publisher landing page and PubMed abstract/metadata | No open legal full text or open legal PDF found. OpenAlex marks closed; Europe PMC marks not OA/no PDF/no PMC. | No legal preprint, author manuscript, or repository copy found during this chase. | Still source-access hold | Crossref exposes an IEEE PDF-like link for publisher workflows, but the access metadata is not open access and this should not be treated as a legal open PDF. |
| RSL-004 | Contactless Sleep Staging With Radar: A Transfer Learning Approach | 10.1109/OJEMB.2026.3667047 | DOI redirect, IEEE Xplore, OpenAlex, Crossref, DOAJ metadata via OpenAlex, TechRxiv preprint DOI, PubMed title search, Semantic Scholar API attempted but rate-limited | Exact IEEE Open Journal of Engineering in Medicine and Biology publisher version | Full publisher version is legal open access. Crossref records CC BY 4.0 for the version of record and points to IEEE Xplore document 11406893. Automated IEEE PDF request was blocked by IEEE anti-bot response, but publisher metadata indicates an OA VOR. | Crossref records `has-preprint` relation to TechRxiv DOI 10.36227/techrxiv.174535565.58795771/v1; TechRxiv DOI resolves to official TechRxiv full page but automated page access was Cloudflare-blocked. | Ready for extraction from exact source | Prefer journal VOR for extraction. Use TechRxiv only as version-linked fallback or comparison if journal page lacks needed method detail. |
| RSL-006 | Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People | 10.1109/TBME.2025.3548780; PMID:40048348 | DOI redirect, IEEE Xplore, PubMed, OpenAlex, Crossref, Europe PMC, arXiv exact-title check, normal web queries for title/PDF/author/institutional copy, Semantic Scholar API attempted but rate-limited | Publisher landing page and PubMed abstract/metadata | No open legal full text or open legal PDF found. OpenAlex marks closed/no repository full text; Europe PMC marks not OA/no PDF/no PMC. | No exact legal preprint or version-linked author manuscript found. RSL-007/arXiv:2601.04057 is related to the same older-adult radar line but has a different title and method framing, so it should not be used as a fallback for extracting RSL-006. | Still source-access hold | Leave on hold unless IEEE access is available through a legal subscription or an author/institutional manuscript is found later. |
| RSL-011 | Deep learning-based automated diagnosis of obstructive sleep apnea and sleep stage classification in children using millimeter-wave radar and pulse oximeter | 10.1016/j.sleh.2025.06.006; PMID:40738779; arXiv:2409.19276 | DOI redirect, Elsevier/Sleep Health PII, PubMed, OpenAlex, Crossref, Europe PMC, arXiv API, normal web queries for title/QSA600/PDF, Semantic Scholar API attempted but rate-limited | Legal arXiv preprint for the same title: arXiv:2409.19276v2 | Exact Sleep Health journal version is not open access in OpenAlex/Europe PMC/Crossref checks. Legal arXiv abstract and PDF are available. | Version-linked fallback exists as arXiv preprint. Crossref did not expose an explicit relation, so use with version/preprint caveat. | Ready only with preprint/version caveat | Extract from the journal version only if legal access appears later. If extraction proceeds now, mark the source as the arXiv preprint/version-linked fallback, not the exact Sleep Health VOR. |
| RSL-013 | Radar-based sleep stage classification in children undergoing polysomnography: a pilot-study | 10.1016/j.sleep.2021.03.022; PMID:33866298 | DOI redirect, Elsevier/Sleep Medicine PII, PubMed, OpenAlex, Crossref, Europe PMC, ScienceDirect landing/PDF endpoints, Erasmus Pure, TU/e Research Portal, Utrecht repository, TU Delft resolver, Semantic Scholar API attempted but rate-limited | Exact publisher version is open under CC BY 4.0; Erasmus Pure repository page also exposes a PDF path | Full legal publisher version confirmed by Crossref/OpenAlex. Erasmus repository page exposes `/files/44028372/1_s2.0_S1389945721001933_main.pdf`; direct automated PDF request was Cloudflare-blocked but the repository landing page parsed the PDF link. | Institutional repository copies found; no separate preprint needed. | Ready for extraction from exact source | ScienceDirect direct automated access was Cloudflare-blocked, but Crossref records CC BY VOR and OpenAlex lists publisher/repository OA locations. |

## Per-source chase notes

### RSL-001

Paper identity:
- Title: Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar
- Journal/source: IEEE Journal of Biomedical and Health Informatics
- DOI/stable IDs: 10.1109/JBHI.2021.3072644; PMID:33848253
- DOI redirect target observed: `https://ieeexplore.ieee.org/document/9403900/`

Search queries used:
- `"Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar" 10.1109/JBHI.2021.3072644`
- `10.1109/JBHI.2021.3072644 IEEE Xplore`
- `"Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar" PubMed`
- `"Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar" Semantic Scholar`
- `"Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar" "author manuscript"`
- `"Attention-Based LSTM for Non-Contact Sleep Stage Classification Using IR-UWB Radar" "pdf" -sci-hub`
- `"Attention-Based LSTM" "IR-UWB" "Seoul National University"`
- `"Attention-Based LSTM" "IR-UWB" "Kwang Suk Park"`

Legal pages checked:
- DOI: `https://doi.org/10.1109/JBHI.2021.3072644`
- IEEE Xplore: `https://ieeexplore.ieee.org/document/9403900/`
- PubMed: `https://pubmed.ncbi.nlm.nih.gov/33848253/`
- OpenAlex: `https://openalex.org/W3153961130`
- Europe PMC: `https://europepmc.org/article/MED/33848253`
- Crossref API record: `https://api.crossref.org/works/10.1109/JBHI.2021.3072644`
- arXiv exact-title query: no entry found
- Semantic Scholar API: attempted, but rate-limited with 429

Legal full text found or not found:
- Not found.
- OpenAlex marks the work as closed and reports no repository full text.
- Europe PMC reports not open access, no PDF, and not in PMC.
- PubMed provides bibliographic/abstract access only.

Version-linked fallback if any:
- None found.

Extraction-readiness decision:
- Still source-access hold.

Unresolved access work:
- Check whether the user's institution has legal IEEE access.
- Re-run author/institutional repository search later, especially Seoul National University, Kwangwoon University, Sangmyung University, and Seoul National University Hospital.
- Re-check Semantic Scholar when rate limits clear.

### RSL-004

Paper identity:
- Title: Contactless Sleep Staging With Radar: A Transfer Learning Approach
- Journal/source: IEEE Open Journal of Engineering in Medicine and Biology
- DOI/stable IDs: 10.1109/OJEMB.2026.3667047; IEEE Xplore document 11406893
- DOI redirect target observed: `https://ieeexplore.ieee.org/document/11406893/`

Search queries used:
- `"Contactless Sleep Staging With Radar: A Transfer Learning Approach" 10.1109/OJEMB.2026.3667047`
- `"Contactless Sleep Staging with Radar: A Transfer Learning Approach" TechRxiv 174535565`
- `"10.36227/techrxiv.174535565.58795771/v1"`
- `"Contactless Sleep Staging with Radar" "TechRxiv" "PDF"`
- PubMed exact-title search for `"Contactless Sleep Staging With Radar"`

Legal pages checked:
- DOI: `https://doi.org/10.1109/OJEMB.2026.3667047`
- IEEE Xplore: `https://ieeexplore.ieee.org/document/11406893/`
- OpenAlex: `https://openalex.org/W7131127778`
- Crossref API record: `https://api.crossref.org/works/10.1109/OJEMB.2026.3667047`
- TechRxiv preprint DOI: `https://doi.org/10.36227/techrxiv.174535565.58795771/v1`
- TechRxiv redirect target observed: `https://www.techrxiv.org/doi/full/10.36227/techrxiv.174535565.58795771/v1`
- Semantic Scholar API: attempted, but rate-limited with 429

Legal full text found or not found:
- Found.
- OpenAlex marks the journal source as open access/gold and lists the best OA location as the DOI/publisher VOR.
- Crossref records a CC BY 4.0 license for the VOR and points to IEEE Xplore as the maintained source.
- Automated `curl` access to IEEE page/PDF returned an anti-bot response, so later extraction should use a normal browser or legal IEEE access.

Version-linked fallback if any:
- Found.
- Crossref records a `has-preprint` relation to TechRxiv DOI 10.36227/techrxiv.174535565.58795771/v1.
- The TechRxiv DOI resolved to the official TechRxiv full page, but automated page access was Cloudflare-blocked.

Extraction-readiness decision:
- Ready for extraction from exact source.

Unresolved access work:
- During extraction, use the IEEE OJEMB VOR in a browser if automated retrieval remains blocked.
- Compare TechRxiv only if the journal VOR lacks needed methods detail.

### RSL-006

Paper identity:
- Title: Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People
- Journal/source: IEEE Transactions on Biomedical Engineering
- DOI/stable IDs: 10.1109/TBME.2025.3548780; PMID:40048348
- DOI redirect target observed: `https://ieeexplore.ieee.org/document/10915572/`

Search queries used:
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar" 10.1109/TBME.2025.3548780`
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar: A Pilot Study in Older People" "PDF" -sci-hub`
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar" "Imperial College" "repository"`
- `"Maowen Yin" "Unobtrusive Sleep Health Assessment" "PDF"`
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar" "PubMed"`
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar" "arXiv"`
- `"Unobtrusive Sleep Health Assessment Using Impulse Radar" "repository"`

Legal pages checked:
- DOI: `https://doi.org/10.1109/TBME.2025.3548780`
- IEEE Xplore: `https://ieeexplore.ieee.org/document/10915572/`
- PubMed: `https://pubmed.ncbi.nlm.nih.gov/40048348/`
- OpenAlex: `https://openalex.org/W4408183386`
- Europe PMC: `https://europepmc.org/article/MED/40048348`
- Crossref API record: `https://api.crossref.org/works/10.1109/TBME.2025.3548780`
- arXiv exact-title query: no entry found
- Semantic Scholar API: attempted, but rate-limited with 429

Legal full text found or not found:
- Not found.
- OpenAlex marks the work as closed and reports no repository full text.
- Europe PMC reports not open access, no PDF, and not in PMC.
- PubMed provides bibliographic/abstract access only.

Version-linked fallback if any:
- No exact version-linked fallback found.
- Related source RSL-007/arXiv:2601.04057 appears to share the older-adult radar line and dataset context, but the title and framing are different. Treat it as a related or companion source, not a fallback version of RSL-006.

Extraction-readiness decision:
- Still source-access hold.

Unresolved access work:
- Check legal IEEE subscription access.
- Re-run repository search later for Imperial College London, UK Dementia Research Institute, University of Surrey, University of Oslo, and author pages.
- Re-check Semantic Scholar when rate limits clear.

### RSL-011

Paper identity:
- Title: Deep learning-based automated diagnosis of obstructive sleep apnea and sleep stage classification in children using millimeter-wave radar and pulse oximeter
- Journal/source: Sleep Health
- DOI/stable IDs: 10.1016/j.sleh.2025.06.006; PMID:40738779; PII:S2352-7218(25)00133-0; arXiv:2409.19276
- DOI redirect target observed: `https://linkinghub.elsevier.com/retrieve/pii/S2352721825001330`

Search queries used:
- `"Deep Learning-Based Automated Diagnosis of Obstructive Sleep Apnea and Sleep Stage Classification in Children" radar pulse oximeter`
- `"Deep Learning-Based Automated Diagnosis of Obstructive Sleep Apnea and Sleep Stage Classification in Children Using Millimeter-Wave Radar and Pulse Oximeter" "arXiv"`
- `"Deep learning-based automated diagnosis" "Sleep Health" "10.1016/j.sleh.2025.06.006"`
- `"Deep learning-based automated diagnosis" "QSA600" "arXiv"`
- `"Deep learning-based automated diagnosis" "QSA600" "PDF"`

Legal pages checked:
- DOI: `https://doi.org/10.1016/j.sleh.2025.06.006`
- Elsevier linking page: `https://linkinghub.elsevier.com/retrieve/pii/S2352721825001330`
- PubMed: `https://pubmed.ncbi.nlm.nih.gov/40738779/`
- OpenAlex: `https://openalex.org/W4412723345`
- Europe PMC: `https://europepmc.org/article/MED/40738779`
- Crossref API record: `https://api.crossref.org/works/10.1016/j.sleh.2025.06.006`
- arXiv abstract: `https://arxiv.org/abs/2409.19276v2`
- arXiv PDF: `https://arxiv.org/pdf/2409.19276v2`
- Semantic Scholar API: attempted, but rate-limited with 429

Legal full text found or not found:
- Exact journal VOR: not found as open access.
- OpenAlex marks the Sleep Health article as closed and reports no repository full text.
- Europe PMC reports not open access, no PDF, and not in PMC.
- Crossref records Elsevier/Sleep Health publisher metadata but no open license for the VOR.
- Legal arXiv full text and PDF found for the same title.

Version-linked fallback if any:
- Legal arXiv preprint fallback found: arXiv:2409.19276v2.
- Crossref did not expose an explicit journal-preprint relation, so use the arXiv source with a version/preprint caveat.

Extraction-readiness decision:
- Ready only with preprint/version caveat.

Unresolved access work:
- Check whether legal access to the exact Sleep Health article is available through a subscription or author/institutional manuscript.
- During extraction, label the source as arXiv preprint unless the journal VOR is accessed legally.
- Re-check Semantic Scholar when rate limits clear.

### RSL-013

Paper identity:
- Title: Radar-based sleep stage classification in children undergoing polysomnography: a pilot-study
- Journal/source: Sleep Medicine
- DOI/stable IDs: 10.1016/j.sleep.2021.03.022; PMID:33866298; PII:S1389-9457(21)00193-3
- DOI redirect target observed: `https://linkinghub.elsevier.com/retrieve/pii/S1389945721001933`

Search queries used:
- `"Radar-based sleep stage classification in children undergoing polysomnography" "ScienceDirect" "PDF"`
- `S1389945721001933 ScienceDirect PDF "Radar-based sleep stage classification"`
- `"S1389945721001933" "cc-by"`
- Repository page checks for Erasmus Pure, TU/e Research Portal, Utrecht University, and TU Delft

Legal pages checked:
- DOI: `https://doi.org/10.1016/j.sleep.2021.03.022`
- Elsevier linking page: `https://linkinghub.elsevier.com/retrieve/pii/S1389945721001933`
- ScienceDirect landing page: `https://www.sciencedirect.com/science/article/pii/S1389945721001933`
- PubMed: `https://pubmed.ncbi.nlm.nih.gov/33866298/`
- OpenAlex: `https://openalex.org/W3151242282`
- Europe PMC: `https://europepmc.org/article/MED/33866298`
- Crossref API record: `https://api.crossref.org/works/10.1016/j.sleep.2021.03.022`
- Erasmus Pure repository page: `https://pure.eur.nl/en/publications/radar-based-sleep-stage-classification-in-children-undergoing-pol/`
- Erasmus Pure PDF path parsed from page: `https://pure.eur.nl/files/44028372/1_s2.0_S1389945721001933_main.pdf`
- TU/e Research Portal: `https://research.tue.nl/en/publications/radar-based-sleep-stage-classification-in-children-undergoing-pol/`
- Utrecht University Repository handle: `https://dspace.library.uu.nl/handle/1874/442665`
- TU Delft resolver: `http://resolver.tudelft.nl/uuid:089e25b0-ea31-4715-bd98-ee141fadb752`
- Semantic Scholar API: attempted, but rate-limited with 429

Legal full text found or not found:
- Found.
- Crossref records CC BY 4.0 for the version of record.
- OpenAlex marks the source as OA/hybrid with publisher and repository locations.
- Erasmus Pure repository page exposes a PDF path for the Elsevier main PDF.
- Automated direct requests to ScienceDirect and the Erasmus PDF endpoint were Cloudflare-blocked, but the legal landing pages and OA metadata are sufficient to mark this source ready.

Version-linked fallback if any:
- Institutional repository copies are available.
- No separate preprint is needed because the exact publisher version is open.

Extraction-readiness decision:
- Ready for extraction from exact source.

Unresolved access work:
- Use a normal browser if automated ScienceDirect/Erasmus PDF requests are blocked.
- Prefer publisher VOR or Erasmus-hosted PDF path during extraction.

## Do-not-use sources

Do not use pirated PDFs, Sci-Hub, random PDF mirrors, unofficial file dumps, or pages that cannot be tied to a publisher, author, institution, repository, DOI, PubMed, arXiv, TechRxiv, Crossref/OpenAlex-style metadata record, or other legal primary/near-primary source.

## Recommended candidate-register updates later

Do not edit the candidate register in this source-access chase.

Proposed later updates:

- RSL-001: keep `P0`; keep `Needs primary-source access first`; set source-access status to `Abstract/metadata only; closed publisher page; no legal full text found in chase`.
- RSL-004: keep `P0`; change extraction readiness to `Ready for extraction`; set source-access status to `Full publisher version available; IEEE OJEMB OA VOR; TechRxiv preprint fallback`.
- RSL-006: keep `P0`; keep `Needs primary-source access first`; set source-access status to `Abstract/metadata only; closed publisher page; no exact preprint/repository copy found`.
- RSL-011: keep `P0`; change extraction readiness to `Ready only with preprint/version caveat`; set source-access status to `Exact Sleep Health VOR closed; legal arXiv preprint/PDF available`.
- RSL-013: keep `P0`; change extraction readiness to `Ready for extraction`; set source-access status to `Full publisher version available; CC BY VOR; institutional repository PDF path found`.

## Extraction gate outcome

### Ready for extraction from exact source

- RSL-004: exact IEEE OJEMB publisher version is open access under CC BY 4.0.
- RSL-013: exact Sleep Medicine publisher version is open under CC BY 4.0; repository PDF path found.

### Ready only with preprint/version caveat

- RSL-011: exact Sleep Health VOR remains closed, but arXiv:2409.19276v2 provides legal full text for the same title.

### Still source-access hold

- RSL-001: no open legal full text or version-linked fallback found.
- RSL-006: no open legal full text or exact version-linked fallback found.

## What to paste back into ChatGPT

Paste either:

- the full new artifact, or
- `git diff -- radar-ml/radar-sleep-stage-literature/raw/v2-source-access-chase-2026-06-13.md`
