# Research Paper Discovery and BibTeX Prompts

Two reusable prompts for finding relevant research papers, checking publication and venue information, and preparing BibTeX references.

## Choose a prompt

| Prompt | Publication scope | DOI policy |
| --- | --- | --- |
| [Prompt 1: Q1 journals only](#prompt-1-q1-journals-only) | Peer-reviewed journal articles meeting your chosen Q1 requirement | Verified DOI required |
| [Prompt 2: Q1 journals and CORE A*/A conferences](#prompt-2-q1-journals-and-core-aa-conferences) | Eligible journals and conferences from the supplied candidate lists | Journal DOI required; conference policy selected by you |

## How to use

1. Choose the prompt that matches your reference requirements.
2. Copy the entire text block using its copy button.
3. Replace every `[BRACKETED FIELD]` with your research details. Update the example years for your search.
4. Attach the materials you name in the prompt: your draft, outline, section plan, demo paper, and/or existing `.bib` file.
5. Paste the completed prompt into a research assistant with web access.

Each prompt is self-contained. The venue lists in Prompt 2 are candidates for verification; they do not assert that every listed venue currently meets the requested rank.

## Prompt 1: Q1 journals only

Use this when your reference list must contain journal articles only.

```text
Act as a scholarly literature researcher. Find a verified, relevant set of recent Q1 journal articles that I can cite in my research paper.

MY RESEARCH DETAILS

- Research paper title: [INSERT MY RESEARCH PAPER TITLE]
- Paper type: [SURVEY / SYSTEMATIC REVIEW / ORIGINAL RESEARCH / OTHER]
- Research objective and intended contribution: [DESCRIBE MY GOAL]
- Target section: [INTRODUCTION / RELATED WORK / SPECIFIC SECTION TITLE / ENTIRE PAPER]
- Topics that must be covered: [LIST TOPICS OR SUBSECTIONS]
- Topics to exclude: [LIST EXCLUSIONS, OR WRITE NONE]
- Number of new papers requested: [FOR EXAMPLE, 25 OR 64]
- Publication year range: [FOR EXAMPLE, 2021–2026]
- Most recent years to prioritize: [FOR EXAMPLE, 2025–2026]
- Q1 requirement: [SCIMAGO SJR Q1 OR CLARIVATE JCR Q1 / JCR Q1 ONLY]
- Allowed journals: [INSERT A SHORTLIST, OR WRITE ANY RELEVANT JOURNAL MEETING THE Q1 RULE]

ATTACHED MATERIALS

I have attached the relevant materials for this task: [LIST MY ATTACHED DRAFT, OUTLINE, SECTION PLAN, DEMO PAPER, AND/OR EXISTING BIBTEX FILE].

Read the attachments before selecting papers. Use them to understand my actual scope, terminology, research questions, and planned contribution. Treat any demo paper as a structural example; do not assume its subject is my subject.

State briefly which attachments you could read and how you interpret my scope. If essential information is missing, ask a focused question; otherwise proceed.

STRICT SELECTION RULES

1. Include peer-reviewed JOURNAL articles only, with a verified DOI. Exclude conference papers, workshop papers, book chapters, editorials, and papers that are only submitted or under review.
2. Exclude preprint versions, including arXiv, SSRN, TechRxiv, and bioRxiv. Do not use ResearchGate uploads as publication evidence. If a preprint has a published journal version, cite only that journal version.
3. Exclude all MDPI and Frontiers journals, including papers with DOI prefix 10.3390.
4. Verify each journal’s Q1 status using the latest available ranking edition under my chosen Q1 requirement. Report the database, ranking year, relevant subject category, and evidence link. If rankings differ, disclose the difference. Do not infer Q1 from the publisher, journal reputation, or impact factor alone.
5. If Q1 status cannot be verified, exclude the paper from the final verified list. If direct ranking-database access is unavailable, identify any public corroborating source accurately and disclose the access limitation.
6. Stay within my publication year range and prioritize the newest relevant articles. Include at most three papers primarily for foundational background, and label those “foundational.” Exclude future-dated or forthcoming records unless a published version is already available.
7. Select papers for their direct relevance and distinct contribution. Do not add loosely related papers merely to reach the requested count. Include a suitable balance of primary research and surveys for my target section.
8. If an existing bibliography is attached, identify overlaps by DOI and title. Do not count existing papers toward the requested number of NEW references. Keep an existing citation key when referring to an existing paper.

VERIFICATION

- Browse the web; do not generate the list from memory alone.
- Use Google Scholar for discovery and cross-checking where accessible. Verify bibliographic metadata against the publisher page and/or publisher-deposited DOI metadata.
- Check the exact title, complete author list, journal, publication year, volume, issue, pages or article number, and DOI.
- Use the final issue metadata when available. Distinguish the online-first date from the final issue year. A DOI’s embedded year does not determine the citation year.
- For genuinely published early-access articles without assigned volume/pages, say “not yet assigned” and omit those fields from BibTeX. Never invent missing values.
- Verify any contribution statement from the abstract or full text. Do not invent experimental results or imply that a survey performed experiments it only reviewed.
- Report Google Scholar verification separately from publisher/DOI verification. If Scholar is blocked, explicitly mark its status “UNVERIFIED—access unavailable”; do not claim it was checked.
- If browsing is unavailable, say so at the top and do not present an unverified list as verified.
- Return fewer papers if necessary. Never relax the rules to reach the requested number.

OUTPUT

First, give a short scope statement and the search date.

Then group the papers by my planned topics or subsections. For EVERY paper provide:

1. A complete, ready-to-use @article BibTeX entry with all verified authors and a unique key in the form firstauthorYEARkeyword.
2. One sentence explaining its main contribution.
3. One sentence explaining why it fits my research and exactly where to cite it in the target section.
4. Journal, publisher, publication year, DOI, and clickable publisher/DOI link.
5. Q1 evidence: database, ranking edition, relevant category, evidence link, and whether the evidence was checked directly or through a public corroborating source.
6. Separate statuses for bibliographic verification and Google Scholar verification, with source links.

Finish with:

- A compact table mapping citation keys to my subsections.
- Counts by publication year and a list of any foundational papers.
- Any verification or access limitations.
- A deduplicated .bib file if file creation is available.

Before submitting, check that every included paper meets the date, journal, DOI, Q1, and relevance requirements; that no DOI or citation key is duplicated; and that every BibTeX entry corresponds to its stated paper.

Do not write the manuscript section yet.
```

## Prompt 2: Q1 journals and CORE A*/A conferences

Use this when eligible journal articles and conference papers are both permitted. Choose `REQUIRED` for the conference DOI policy if every reference must have a DOI.

```text
Act as a careful academic research assistant. Find verified, relevant, peer-reviewed papers for my research paper and provide ready-to-use BibTeX entries. Include only eligible Q1 journal articles and CORE A* or A conference papers from the candidate venues below.

MY RESEARCH DETAILS

- Research paper title: [INSERT MY RESEARCH PAPER TITLE]
- Topic, keywords, and sub-area: [INSERT MY TOPIC / KEYWORDS / SUB-AREA]
- Paper type: [SURVEY / SYSTEMATIC REVIEW / ORIGINAL RESEARCH / OTHER]
- Research objective and intended contribution: [DESCRIBE MY GOAL]
- Target section: [INTRODUCTION / RELATED WORK / SPECIFIC SECTION TITLE / ENTIRE PAPER]
- Topics that must be covered: [LIST TOPICS OR SUBSECTIONS]
- Topics to exclude: [LIST EXCLUSIONS, OR WRITE NONE]
- Number of new papers requested: [FOR EXAMPLE, 15–20, 25, OR 64]
- Publication year range: [FOR EXAMPLE, 2021–2026]
- Most recent years to prioritize: [FOR EXAMPLE, 2025–2026]
- Maximum foundational papers within the allowed range: [FOR EXAMPLE, 2 OR 3]
- Journal Q1 requirement: [SCIMAGO SJR Q1 OR CLARIVATE JCR Q1 / JCR Q1 ONLY]
- Conference DOI policy: [REQUIRED / PREFERRED]

ATTACHED MATERIALS

I have attached the relevant materials for this task: [LIST MY ATTACHED DRAFT, OUTLINE, SECTION PLAN, DEMO PAPER, AND/OR EXISTING BIBTEX FILE].

Read the attachments before searching. Use them to understand my scope, research questions, terminology, and intended contribution. A demo paper shows the desired structure; its subject must not replace my actual topic.

Briefly state which attachments you could read and your interpretation of my scope. Ask a focused question only if essential information is missing; otherwise proceed.

STRICT SELECTION RULES

1. Include peer-reviewed journal articles or accepted, published main-conference papers only. Exclude unpublished submissions, papers only under review, workshop papers, editorials, and book chapters.
2. Exclude preprint versions, including arXiv, SSRN, TechRxiv, and bioRxiv. Do not use ResearchGate uploads as publication evidence. If a published version exists, cite that version only. For OpenReview-hosted papers, verify acceptance at the eligible conference; an OpenReview page alone is not proof of acceptance.
3. Exclude every MDPI and Frontiers journal, including DOI prefix 10.3390.
4. Journals must satisfy my chosen Q1 requirement in the latest available ranking edition. Verify the database, ranking year, relevant subject category, and evidence link. Disclose conflicting rankings and whether the evidence was checked directly or through a public corroborating source.
5. Conferences must be CORE A* or A in the latest available CORE conference ranking. Verify the exact venue name, ranking edition, rank, and source link. Do not transfer a main-conference rank to a workshop or an unrelated track.
6. The candidate lists below are search constraints, not guarantees of current rank. Exclude any venue whose qualifying rank cannot be verified. Do not infer eligibility from reputation, publisher, impact factor, or inclusion in the list.
7. Journal articles must have a verified DOI. Apply my selected conference DOI policy:
   - REQUIRED: exclude conference papers without a verified DOI.
   - PREFERRED: prioritize papers with verified DOIs; allow a paper without one only when its published official record is verified and no DOI is assigned. Report “No DOI assigned—official proceedings verified.” Exclude papers when DOI existence remains uncertain.
8. Stay within my year range and prioritize my selected recent years. Use no more than my specified maximum of foundational papers, all within the allowed range, and label them “foundational.” Exclude future-dated or forthcoming records unless a published version is already available.
9. Select papers for direct relevance and distinct contributions. Do not fill the list with loosely related papers. If an existing bibliography is attached, deduplicate by DOI and title, retain existing citation keys, and do not count existing references as new papers.
10. Return fewer papers if necessary. Do not relax any rule to reach the requested count.

CANDIDATE JOURNALS — VERIFY CURRENT Q1 ELIGIBILITY

- ML/DL/AI: IEEE TPAMI; JMLR; Artificial Intelligence; JAIR; Machine Learning; IEEE TNNLS; Neural Networks; Nature Machine Intelligence.
- Vision: IJCV; IEEE TIP; CVIU; Pattern Recognition; IEEE TCSVT; Medical Image Analysis; IEEE TMI; IEEE TGRS; ISPRS Journal of Photogrammetry and Remote Sensing.
- General CS/Engineering: JACM; ACM Computing Surveys; IEEE TKDE; ACM TOIS; IEEE TSE; ACM TOSEM; IEEE TC; ACM TOCS; IEEE TPDS; IEEE/ACM ToN; IEEE TDSC; IEEE TIFS; Journal of Cryptology; ACM TOG; IEEE TVCG; ACM TOCHI; TACL; Computational Linguistics; IEEE/ACM TASLP; IEEE T-RO; IJRR; IEEE TSP; IEEE TCYB; IEEE TII; Information Fusion.

CANDIDATE CONFERENCES — VERIFY CURRENT CORE A*/A ELIGIBILITY

- ML: NeurIPS; ICML; ICLR; AISTATS; UAI; COLT; MLSys.
- AI: AAAI; IJCAI.
- Vision: CVPR; ICCV; ECCV; WACV.
- NLP/LLM: ACL; EMNLP; NAACL; EACL.
- Robotics: ICRA; IROS; RSS; CoRL.
- Data mining/Web: KDD; WWW; WSDM; ICDM.
- Security: IEEE S&P; USENIX Security; ACM CCS; NDSS.
- Networking: SIGCOMM; NSDI; MobiCom; INFOCOM; SIGMETRICS.
- Mobile/Sensing: SenSys; MobiSys; PerCom.
- Systems: SOSP; OSDI; EuroSys; ASPLOS; USENIX ATC; FAST.
- Databases: SIGMOD; VLDB; ICDE.
- Software Engineering: ICSE; FSE; ASE.
- HCI: CHI; UIST; CSCW.
- Theory: STOC; FOCS; SODA.
- Programming Languages: POPL; PLDI; OOPSLA.
- Architecture/EDA: ISCA; MICRO; HPCA; DAC; ICCAD.
- Graphics: SIGGRAPH; SIGGRAPH Asia.
- Cryptography: CRYPTO; EUROCRYPT; ASIACRYPT.
- Information Retrieval: SIGIR.
- Social Computing: ICWSM.
- Multimedia: ACM MM.
- Bioinformatics: ISMB; RECOMB.
- Speech/Signal: ICASSP; INTERSPEECH.
- Verification: CAV.

ALLOWED PUBLISHERS AND OFFICIAL PUBLICATION SOURCES

IEEE; ACM; Springer Nature, including Nature Portfolio; Elsevier; Wiley; Taylor & Francis; SAGE; PMLR; NeurIPS Proceedings; CVF Open Access; ACL Anthology; AAAI; IJCAI; USENIX; OpenReview for accepted papers only.

For journals explicitly named in the candidate list, their official publishing bodies are also allowed. These source names do not replace the Q1/CORE and publication-status checks.

VERIFICATION

- Browse the web. Do not produce the bibliography from memory alone.
- Use Google Scholar for discovery and cross-checking where accessible. Verify metadata against official publisher/proceedings records and/or publisher-deposited DOI metadata.
- Verify the exact title, full author list, venue, publication year, volume, issue, pages or article number, and DOI where assigned.
- Use the final publication metadata when available. Distinguish online-first dates from final issue years; do not infer a publication year from the DOI string.
- Never invent a missing field. For published early-access papers, report unassigned fields as “not yet assigned” outside BibTeX and omit those fields from the entry. Mark genuinely uncertain information “UNVERIFIED”; exclude the paper if the uncertainty affects an eligibility requirement.
- Verify contribution statements using the abstract or full text. Do not invent numerical results or describe a review as an experimental study.
- Report publisher/proceedings verification, ranking verification, and Google Scholar verification separately.
- If Google Scholar is blocked, report “UNVERIFIED—access unavailable” for that check. Do not claim Scholar verification based on another source.
- If browsing is unavailable, say so at the top and do not present an unverified list as verified.

OUTPUT

Start with my interpreted scope and the search date. Group papers by sub-theme or planned subsection.

For EVERY paper provide:

1. A complete, ready-to-use BibTeX entry with all verified authors and a unique firstauthorYEARkeyword key. Use @article for journal records and @inproceedings for proceedings records. If a conference-associated paper is published in a journal series, follow the publisher’s actual record type and explain the eligibility route.
2. One sentence explaining the main contribution.
3. One sentence explaining its relevance to my research and exactly where to cite it.
4. Venue, publisher or official proceedings source, publication year, DOI or verified no-DOI status, and an official publication link.
5. Ranking evidence:
   - Journal: Q1 database, ranking edition, relevant category, and evidence link.
   - Conference: CORE rank, ranking edition, exact venue name, and evidence link.
6. Separate verification statuses for bibliographic metadata, venue ranking, and Google Scholar, with source links.

Finish with:

- A table mapping citation keys to my subsections.
- Counts by year and publication type, plus any foundational papers.
- A list of requested sub-themes or evidence gaps you could not fill.
- Any verification or access limitations.
- A deduplicated .bib file if file creation is available.

Perform a final check for relevance, eligibility, publication dates, valid metadata, duplicate DOIs, and duplicate citation keys. Do not write the manuscript section yet.
```

## Educational use and credit

These prompts, infographics, and this guide are shared for educational purposes. Feel free to reference or adapt the structure for your own writing; please credit the author if reposting the visuals themselves.

## Author

**Irfanul Kabir Hira**

Feel free to connect for feedback, collaboration, or questions about the structures used here.
