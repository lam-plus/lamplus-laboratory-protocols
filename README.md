<p align="center">
  <img src="assets/branding/logo-lamplus-transparent.png" alt="LAM+ logo" width="280">
</p>

# LAM+ Laboratory Protocols

[English](README.md) | [Português](README.pt-BR.md)

This repository contains the public, version-controlled operating protocols of the **LAM+ Multi-User Laboratory** at **Universidade Federal Fluminense (UFF), Brazil**.

The project provides clear, reproducible, and openly accessible guidance for operating LAM+ analytical systems. Protocols are maintained as bilingual Markdown documents in English and Brazilian Portuguese and are designed to generate standardized PDF documents with Pandoc.

## Current scope

The repository currently covers three laboratory systems:

| System | Description | Protocol status |
|---|---|---|
| [HSI scanning system](equipment/hsi-scanning-system/) | Integrated hyperspectral scanning system, including cameras, illumination, translation stage, reference targets, control software, calibration, acquisition, and data handling | Protocol development not yet started |
| [Avaatech XRF Core Scanner](equipment/avaatech-xrf-core-scanner/) | X-ray fluorescence core-scanning system | Existing Word protocol awaiting migration to Markdown |
| [SEM–EDS](equipment/mev-eds/) | Scanning electron microscopy with energy-dispersive X-ray spectroscopy | Protocol development not yet started |

Additional instruments may be included after their scope, documentation requirements, and technical responsibilities have been defined.

## Documentation workflow

Markdown files are the authoritative editable sources. The intended publication workflow is:

```text
Markdown → technical review → Pandoc PDF → GitHub Release → Zenodo
```

English and Portuguese versions of the same protocol share the same identifier, version, approval status, and technical content. PDF files are generated outputs and should not be edited directly.

Versioned releases will be archived in **Zenodo** to provide permanent access and citable records. The first Zenodo publication has not yet been released and will be announced here when available.

## Repository organization

```text
equipment/              Equipment-specific protocols and images
templates/              Bilingual Markdown and Pandoc templates
assets/branding/        LAM+ and institutional branding assets
TODO.md                 Development and publication roadmap
CHANGELOG.md            Changes included in repository releases
AGENTS.md               Repository instructions for coding agents
```

Equipment-specific images are stored alongside the corresponding system. Shared visual identity files are kept in `assets/branding/`.

## Protocols and manufacturer manuals

These documents are **LAM+ operating protocols**, developed for the systems installed and used at the laboratory. They are not copies or replacements for manufacturer manuals.

Manufacturer documentation remains an important technical reference. Users must consult the applicable manufacturer instructions whenever required, particularly for safety limits, maintenance, regulated activities, and procedures not covered by a LAM+ protocol.

## Contributing

Suggestions, corrections, translations, and technical improvements are welcome through GitHub issues and pull requests.

Public access does not mean that proposed changes are automatically accepted. Changes affecting operating procedures, calibration, safety, instrument settings, or quality-control criteria require review by the appropriate LAM+ technical maintainers before approval.

Before contributing, please:

1. check the relevant equipment directory and `TODO.md`;
2. preserve the bilingual organization;
3. use relative paths for images and internal links;
4. provide the source and licensing information for contributed images;
5. avoid adding proprietary manuals, confidential information, credentials, personal data, or unverified instrument settings.

Detailed contribution guidelines will be maintained in `CONTRIBUTING.md`.

## Document status and safety

Protocols may be marked as `Draft`, `Under review`, `Approved`, `Superseded`, or `Retired`. Only documents explicitly marked as **Approved** should be treated as authorized LAM+ operating procedures.

Users remain responsible for following laboratory training requirements, institutional safety rules, radiation-protection requirements, manufacturer instructions, and applicable regulations. A public protocol does not replace equipment-specific authorization or supervised training.

## License and attribution

Unless otherwise stated, original protocol documentation is intended for release under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

Institutional names, logos, and trademarks are not automatically covered by the documentation license. Third-party materials retain their respective ownership and licensing conditions.

Citation information will be provided through `CITATION.cff` and the future Zenodo record.

## Contact

Questions, suggestions, and requests for additional information may be submitted through this repository's GitHub issue tracker or sent directly to:

- **Igor Venancio:** [ivenancio@id.uff.br](mailto:ivenancio@id.uff.br)
- **André Belém:** [andrebelem@id.uff.br](mailto:andrebelem@id.uff.br)

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.

## License

Unless otherwise indicated, the original content of this repository is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE).

Third-party images, trademarks, software, manuals, and other externally sourced materials remain subject to their respective licenses and terms of use.
