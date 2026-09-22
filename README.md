# LAM+ — Laboratory protocols

[Português brasileiro](README.pt-BR.md)

Public, open repository of operating protocols for the LAM+ Multi-User Laboratory, Universidade Federal Fluminense (UFF). Version-controlled Markdown is the editable source of truth. These are LAM+ operating protocols, not copies of manufacturer manuals.

This initial repository provides the documentation framework; no approved operating protocols are available yet.

## Systems

- [HSI scanning system](equipment/hsi-scanning-system/README.md)
- [Avaatech XRF Core Scanner](equipment/avaatech-xrf-core-scanner/README.md)
- [SEM–EDS](equipment/mev-eds/README.md)

## Publication workflow

Markdown → Pandoc → PDF → GitHub Release → Zenodo. Before formal release: complete technical review, synchronize languages, validate links and images, build and inspect both PDFs, update revision histories, and confirm citation and archive metadata. PDFs are release artifacts and should not be added to source directories.

English and Brazilian Portuguese have equal documentary status and share identifiers, versions, dates, and technical content.

## Templates and PDF builds

[Protocol template](templates/protocol-template.md) · [AGENTS.md](AGENTS.md)

Run from the repository root. Tested with Pandoc 3.9 and XeLaTeX. Dependencies: Pandoc 3.9 or later and XeLaTeX, with the TeX packages fontspec, polyglossia (English and Portuguese), geometry, graphicx, longtable, booktabs, array, calc, etoolbox, amsmath, amssymb, xcolor, and hyperref. No pandoc-crossref is required. Syntax highlighting is disabled. Captioned figures and tables use native Pandoc support; automatic cross-references are not configured.

```sh
pandoc --defaults=templates/defaults-en.yaml templates/protocol-template.md -o /tmp/lam-template-en.pdf
pandoc --defaults=templates/defaults-pt-BR.yaml templates/protocol-template.pt-BR.md -o /tmp/lam-template-pt-BR.pdf
```

For real protocols, add `--resource-path=.:equipment/<system>/protocols` to resolve images relative to the protocol. Replace placeholders before review; the template date records scaffold creation only, not publication.

## License and metadata

Documentation and original protocol figures use CC BY 4.0; licensing for software, automation, and LaTeX templates remains to be defined. Institutional branding and third-party materials require their own permission. See [LICENSE](LICENSE).

[CITATION.cff](CITATION.cff) · [.zenodo.json](.zenodo.json) · [CHANGELOG.md](CHANGELOG.md)

TODO: confirm citation authors/contributors, reviewers, release metadata, and software licensing. No DOI or publication date has been assigned. Do not submit placeholder metadata to Zenodo.
