# LAM+ Protocols Repository Instructions

## 1. Purpose

This repository contains the public, version-controlled operating protocols of the LAM+ Multi-User Laboratory at Universidade Federal Fluminense (UFF).

The repository is the authoritative source for editable protocol content. Protocols are written in Markdown, converted to PDF with Pandoc, published as versioned GitHub releases, and archived in Zenodo when formally released.

The initial scope covers only these three systems:

1. HSI scanning system
2. Avaatech XRF Core Scanner
3. MEV–EDS, referred to as SEM–EDS in English documents

Do not introduce additional instruments or reorganize the scope without explicit approval from the repository maintainers.

## 2. Language policy

All public protocols must be available in both English and Brazilian Portuguese.

- English files use the standard `.md` suffix, for example `acquisition.md`.
- Brazilian Portuguese files use `.pt-BR.md`, for example `acquisition.pt-BR.md`.
- `README.md` is the English entry point.
- `README.pt-BR.md` is the Portuguese entry point.
- Each language version must link to its counterpart near the top of the document.
- Both versions represent the same protocol and must use the same protocol identifier, version number, date, status, and substantive technical content.
- English and Portuguese have equal documentary status. English is used for the default filenames to support international discovery.
- Do not place both complete language versions in the same Markdown file.

When changing technical content in one language, update the corresponding file in the other language in the same pull request whenever possible. If synchronization cannot be completed immediately, mark the untranslated document clearly as outdated and open an issue.

## 3. Repository structure

Use the following top-level organization:

```text
Protocols/
├── README.md
├── README.pt-BR.md
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── .zenodo.json
├── AGENTS.md
├── CLAUDE.md
├── templates/
│   ├── protocol-template.md
│   ├── protocol-template.pt-BR.md
│   ├── pdf-template.tex
│   ├── defaults-en.yaml
│   └── defaults-pt-BR.yaml
├── assets/
│   └── branding/
└── equipment/
    ├── hsi-scanning-system/
    │   ├── README.md
    │   ├── README.pt-BR.md
    │   ├── protocols/
    │   └── assets/
    │       ├── common/
    │       ├── en/
    │       └── pt-BR/
    ├── avaatech-xrf-core-scanner/
    │   ├── README.md
    │   ├── README.pt-BR.md
    │   ├── protocols/
    │   └── assets/
    │       ├── common/
    │       ├── en/
    │       └── pt-BR/
    └── mev-eds/
        ├── README.md
        ├── README.pt-BR.md
        ├── protocols/
        └── assets/
            ├── common/
            ├── en/
            └── pt-BR/
```

The HSI entry represents the complete hyperspectral scanning system, not only its cameras. It may include the FX10 and SWIR cameras, illumination, translation stage, reference targets, control software, calibration, acquisition, data handling, and integrated scanning workflow. FX10 and SWIR are components of the HSI scanning system and must not be presented as independent top-level equipment.

## 4. Protocol identifiers

Use stable institutional identifiers:

- `LAM-HSI-###` for the HSI scanning system
- `LAM-XRF-###` for the Avaatech XRF Core Scanner
- `LAM-MEV-###` for MEV–EDS/SEM–EDS

Identifiers must not change when a document is translated or revised. English and Portuguese versions of the same protocol share one identifier.

Use semantic versioning for released documents where practical:

- patch change: typographical, formatting, or other non-substantive correction;
- minor change: clarification or compatible procedural improvement;
- major change: change that materially affects the procedure, outputs, safety, calibration, or interpretation.

Drafts begin at `0.x`. The first formally approved protocol is released as `1.0.0`.

## 5. Required protocol metadata

Every protocol must begin with Pandoc-compatible YAML metadata. At minimum, include:

```yaml
---
title: "Protocol title"
subtitle: "Standard Operating Procedure"
protocol_id: "LAM-HSI-001"
version: "0.1.0"
date: "YYYY-MM-DD"
language: "en"
authors:
  - name: "Author name"
    affiliation: "LAM+, Universidade Federal Fluminense"
reviewers: []
equipment: "HSI scanning system"
status: "Draft"
license: "CC BY 4.0"
keywords: []
---
```

Use ISO dates (`YYYY-MM-DD`). For Portuguese documents, use `language: "pt-BR"`, translate human-readable fields, and preserve the same identifier, version, date, authors, and reviewers.

## 6. Standard protocol sections

Use the shared templates and preserve the following logical sections unless a documented exception is necessary:

1. Purpose and scope
2. Responsibilities and required training
3. Safety requirements
4. Equipment, software, and materials
5. Sample requirements and preparation
6. Instrument or system setup
7. Calibration and reference measurements
8. Acquisition or operating procedure
9. Quality control and acceptance criteria
10. Data organization, file naming, and metadata
11. Shutdown, cleaning, and routine care
12. Troubleshooting
13. References and related documents
14. Revision history

Write protocols as executable laboratory procedures. Distinguish mandatory actions, recommendations, warnings, expected results, and troubleshooting guidance.

## 7. Markdown and Pandoc compatibility

Markdown is the authoritative editable format. PDFs are generated artifacts and must not be edited directly.

- Use Pandoc-compatible Markdown.
- Keep the Markdown readable in the GitHub interface.
- Prefer standard Markdown constructs over embedded HTML.
- Avoid raw LaTeX unless the same result cannot reasonably be obtained through the shared template or Pandoc configuration.
- Use relative paths for local images and other repository resources.
- Do not use absolute filesystem paths.
- Do not use external image URLs for required protocol content.
- Keep headings hierarchical; do not skip heading levels without reason.
- Use tables only when they remain legible in both GitHub and the generated PDF.
- Verify that every edited protocol can be converted using the repository's documented Pandoc workflow.

The shared `pdf-template.tex` controls the PDF visual identity, including cover, fonts, margins, headers, footers, logos, page numbering, and protocol metadata. The Markdown files should focus on content rather than page-specific formatting.

Language-specific Pandoc defaults belong in `templates/defaults-en.yaml` and `templates/defaults-pt-BR.yaml`.

## 8. Images and other assets

Store equipment-specific images with the relevant equipment:

- `assets/common/`: photographs, plots, and diagrams without language-specific text;
- `assets/en/`: screenshots and diagrams containing English text;
- `assets/pt-BR/`: screenshots and diagrams containing Portuguese text;
- top-level `assets/branding/`: shared institutional logos and visual identity assets.

Use image references relative to the Markdown file. Example:

```markdown
![Specim FX10 camera and illumination system.](../assets/common/fx10-overview.jpg){#fig-fx10-overview width=85%}
```

The Portuguese counterpart may reuse the same image with a translated caption:

```markdown
![Câmera Specim FX10 e sistema de iluminação.](../assets/common/fx10-overview.jpg){#fig-fx10-overview width=85%}
```

Asset rules:

- use lowercase, descriptive, hyphen-separated filenames;
- do not use spaces, accents, or ambiguous names such as `image1.png`;
- use JPEG for photographs and PNG for screenshots;
- prefer vector PDF or SVG sources for diagrams and scientific graphics;
- retain editable source files for original diagrams when available;
- provide sufficient resolution for the intended PDF size, normally about 300 dpi for raster images;
- include informative alternative text and a concise caption;
- do not commit unnecessary duplicate images;
- record authorship, source, date, and license in the equipment's `assets/IMAGE_CREDITS.md`.

Do not copy figures, screenshots, or substantial text from manufacturer manuals unless the license or explicit permission allows republication. Prefer original LAM+ photographs, screenshots, and diagrams. Manuals may be cited and linked as references without being republished.

## 9. Manufacturer manuals and technical sources

Manufacturer manuals are reference sources, not substitutes for LAM+ protocols.

- Do not reproduce a manual as a protocol.
- Extract only the information required to define the laboratory procedure.
- Clearly distinguish manufacturer specifications from LAM+ decisions and validated laboratory practices.
- Cite the manual version and relevant section or page where useful.
- Flag any value that has not yet been verified on the installed equipment.
- Never invent settings, safety limits, calibration parameters, or acceptance criteria.

If the available documentation conflicts with observed equipment behavior, record the discrepancy and request technical review before publishing instructions.

## 10. Scientific, technical, and safety quality

- Base procedural claims on manuals, verified laboratory experience, validated tests, or cited technical sources.
- Preserve units exactly and use SI units whenever appropriate.
- State instrument-specific settings with their units and applicable conditions.
- Identify steps that may damage samples, instruments, detectors, X-ray components, vacuum systems, or calibration materials.
- Highlight radiation, electrical, vacuum, mechanical, chemical, biological, and sample-contamination hazards as applicable.
- Do not convert uncertain observations into mandatory instructions.
- Mark unresolved information with a visible `TODO`, issue reference, or draft warning.
- Protocols involving ionizing radiation, vacuum systems, high voltage, or other regulated hazards require review by an appropriately qualified person before formal release.

## 11. Data and file-management guidance

Protocols should define, when applicable:

- required sample and project identifiers;
- file and directory naming conventions;
- raw, intermediate, and processed data separation;
- instrument-generated metadata that must be preserved;
- calibration and quality-control records;
- approved export formats;
- backup destination and minimum retention expectations;
- transformations that must be documented for reproducibility.

Never place research data, personal data, confidential project information, credentials, license keys, or sensitive network details in this public repository.

## 12. Review and publication workflow

Use the following states:

- `Draft`: incomplete or under active development;
- `Under review`: technically complete and awaiting review;
- `Approved`: reviewed and authorized for laboratory use;
- `Superseded`: replaced by a newer protocol or workflow;
- `Retired`: no longer applicable and not replaced directly.

Before an approved release:

1. confirm technical review;
2. synchronize the English and Portuguese versions;
3. validate all internal links and image paths;
4. build both PDFs with Pandoc;
5. inspect the PDFs visually for missing figures, overflow, broken tables, incorrect page breaks, and metadata errors;
6. update `CHANGELOG.md` and revision histories;
7. confirm citation and Zenodo metadata;
8. create a tagged GitHub release;
9. archive the formal release in Zenodo.

Do not commit generated PDFs to ordinary source directories unless the maintainers explicitly decide to version them. Prefer attaching generated PDFs to GitHub releases and Zenodo records.

## 13. Citation, licensing, and attribution

Documentation and original protocol figures should normally be released under `CC BY 4.0`. Code, build scripts, and automation may use the repository's selected software license, such as MIT or BSD-3-Clause.

Maintain:

- `CITATION.cff` for GitHub citation support;
- `.zenodo.json` for Zenodo metadata when used;
- ORCID identifiers where available;
- complete contributor and affiliation information;
- an explicit distinction between documentation licensing and software licensing.

Do not assign a DOI manually. Use the DOI created or reserved through the approved Zenodo publication workflow.

## 14. Working practices for coding agents

Before making changes:

1. read this file and the nearest applicable repository instructions;
2. inspect the existing templates and relevant equipment directory;
3. preserve user-authored work and unrelated changes;
4. verify facts against the available technical sources;
5. ask for clarification when a choice would materially change scientific, safety, licensing, or publication outcomes.

When editing:

- make focused, reviewable changes;
- preserve bilingual pairing and protocol identifiers;
- do not silently rename or move published protocol files;
- do not delete superseded protocols without explicit approval;
- do not fabricate missing images or technical details;
- avoid broad mechanical rewrites that alter technical meaning;
- update navigation files when adding, moving, or renaming protocols;
- keep GitHub rendering and Pandoc output compatible.

When reporting work, summarize changed files, validation performed, unresolved issues, and any content requiring expert review.

## 15. Claude Code compatibility

`AGENTS.md` is the canonical instruction file. The repository-level `CLAUDE.md` should contain:

```markdown
@AGENTS.md
```

Do not duplicate these instructions in `CLAUDE.md`. This keeps Codex and Claude Code aligned with one maintained source of repository guidance.

