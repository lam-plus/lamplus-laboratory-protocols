# LAM+ Protocols — TODO

This file tracks the development, review, translation, validation, and publication of the LAM+ operating protocols.

Completed and formally released work must be recorded in `CHANGELOG.md`. This file should contain only pending or ongoing tasks.

## Current status

| System                    | Existing source              | English Markdown | Portuguese Markdown | Technical review | PDF validation | Status                        |
| ------------------------- | ---------------------------- | ---------------: | ------------------: | ---------------: | -------------: | ----------------------------- |
| Avaatech XRF Core Scanner | Established protocol in Word |      Not started |         Not started |          Pending |        Pending | Migration required            |
| HSI scanning system       | No protocol yet              |      Not started |         Not started |          Pending |        Pending | Protocol development required |
| MEV–EDS / SEM–EDS         | No protocol yet              |      Not started |         Not started |          Pending |        Pending | Protocol development required |

## Repository infrastructure

* [ ] Confirm the final repository structure.
* [ ] Review the English and Portuguese protocol templates.
* [ ] Review the Pandoc LaTeX template.
* [ ] Validate `defaults-en.yaml`.
* [ ] Validate `defaults-pt-BR.yaml`.
* [ ] Confirm the documentation license.
* [ ] Define the license for scripts and build automation.
* [ ] Complete and validate `CITATION.cff`.
* [ ] Complete and validate `.zenodo.json`.
* [ ] Add the official LAM+ and UFF branding assets.
* [ ] Define the GitHub Release workflow.
* [ ] Define the Zenodo publication workflow.
* [ ] Decide whether PDF generation will be manual, automated with GitHub Actions, or both.
* [ ] Add link validation and Markdown checks.
* [ ] Test English and Portuguese PDF generation.

## Avaatech XRF Core Scanner

Priority: **High**

An established protocol already exists in Microsoft Word and must be migrated to the repository without changing its technical meaning.

### Source assessment

* [ ] Locate and add the authoritative Word protocol to the controlled working area.
* [ ] Confirm the document title, authors, date, and current version.
* [ ] Identify the latest approved Word version.
* [ ] Identify embedded images, tables, captions, and appendices.
* [ ] Identify references to manufacturer documentation.
* [ ] Identify information that is outdated, uncertain, or specific to an earlier configuration.
* [ ] Record unresolved questions before conversion.

### Conversion to Markdown

* [ ] Convert the Word document to structured Markdown.
* [ ] Preserve the original procedural sequence.
* [ ] Map the content to the standard LAM+ protocol sections.
* [ ] Extract images from the Word document.
* [ ] Rename image files using lowercase, descriptive, hyphen-separated names.
* [ ] Place reusable images in `assets/common/`.
* [ ] Place language-specific images in `assets/en/` or `assets/pt-BR/`.
* [ ] Create or update `assets/IMAGE_CREDITS.md`.
* [ ] Rebuild tables in Pandoc-compatible Markdown.
* [ ] Add Pandoc-compatible captions and figure identifiers.
* [ ] Check internal links and relative image paths.
* [ ] Assign a definitive `LAM-XRF-###` identifier after confirming the protocol scope.

### Bilingual preparation

* [ ] Establish the authoritative Portuguese Markdown version from the existing Word protocol.
* [ ] Prepare the corresponding English version.
* [ ] Verify that both versions contain equivalent technical instructions.
* [ ] Ensure that identifiers, versions, dates, authors, and reviewers match.
* [ ] Add reciprocal language links.

### Validation and publication

* [ ] Perform technical review against the installed Avaatech configuration.
* [ ] Verify all operating parameters and units.
* [ ] Verify safety and radiation-protection information.
* [ ] Compare the protocol with the applicable manufacturer manual.
* [ ] Build the English PDF.
* [ ] Build the Portuguese PDF.
* [ ] Perform visual PDF inspection.
* [ ] Correct layout, figure, table, and page-break problems.
* [ ] Change document status from `Draft` only after formal review.
* [ ] Add the approved protocol to a versioned GitHub Release.
* [ ] Archive the approved release in Zenodo.

## HSI scanning system

Priority: **Medium**

The protocol must describe the complete hyperspectral scanning system, not only the individual cameras.

### Scope definition

* [ ] Define the complete HSI system boundary.
* [ ] Inventory the installed components.
* [ ] Document the role of the FX10 camera.
* [ ] Document the role of the SWIR camera.
* [ ] Document illumination components.
* [ ] Document the translation stage and movement control.
* [ ] Document reference targets and calibration materials.
* [ ] Identify acquisition and control software.
* [ ] Define supported sample types and intended applications.
* [ ] Identify safety considerations.
* [ ] Define raw-data and metadata outputs.

### Protocol planning

* [ ] Decide whether the HSI documentation will use one integrated protocol or several linked protocols.
* [ ] Define the startup and shutdown workflow.
* [ ] Define system inspection and pre-use checks.
* [ ] Define sample preparation requirements.
* [ ] Define geometric setup and camera positioning.
* [ ] Define illumination stabilization procedures.
* [ ] Define reference and calibration measurements.
* [ ] Define FX10 acquisition procedures.
* [ ] Define SWIR acquisition procedures.
* [ ] Define integrated scanning procedures.
* [ ] Define quality-control and acceptance criteria.
* [ ] Define data naming, storage, backup, and metadata requirements.
* [ ] Define routine cleaning and care.
* [ ] Create an initial troubleshooting section.

### Documentation and validation

* [ ] Create original photographs and diagrams of the installed system.
* [ ] Record image authorship and licensing.
* [ ] Draft the Portuguese protocol or protocol set.
* [ ] Prepare the corresponding English version.
* [ ] Perform technical review on the installed system.
* [ ] Run a complete test acquisition using the written procedure.
* [ ] Revise the protocol based on the test.
* [ ] Build and inspect both language PDFs.
* [ ] Approve and publish the first release.

## MEV–EDS / SEM–EDS

Priority: **Medium**

Use “MEV–EDS” in Portuguese and “SEM–EDS” in English.

### Scope definition

* [ ] Confirm the installed instrument model and configuration.
* [ ] Inventory detectors, holders, accessories, and software.
* [ ] Define permitted sample types.
* [ ] Define sample-size and preparation requirements.
* [ ] Document coating requirements, when applicable.
* [ ] Identify vacuum, high-voltage, contamination, and sample hazards.
* [ ] Define image-acquisition outputs.
* [ ] Define EDS-analysis outputs and metadata.

### Protocol planning

* [ ] Define startup and pre-use inspection.
* [ ] Define sample mounting and loading.
* [ ] Define vacuum operation.
* [ ] Define imaging workflow.
* [ ] Define EDS acquisition workflow.
* [ ] Define calibration and reference checks.
* [ ] Define quality-control and acceptance criteria.
* [ ] Define data export and file naming.
* [ ] Define shutdown, cleaning, and routine care.
* [ ] Create an initial troubleshooting section.

### Documentation and validation

* [ ] Create original photographs and diagrams.
* [ ] Record image authorship and licensing.
* [ ] Draft the Portuguese protocol or protocol set.
* [ ] Prepare the corresponding English version.
* [ ] Perform technical review on the installed system.
* [ ] Test the complete written procedure.
* [ ] Revise the protocol based on the test.
* [ ] Build and inspect both language PDFs.
* [ ] Approve and publish the first release.

## Publication milestones

* [ ] Repository scaffold reviewed.
* [ ] Pandoc workflow validated.
* [ ] First Avaatech Markdown draft completed.
* [ ] Avaatech bilingual technical review completed.
* [ ] Avaatech protocol v1.0.0 released.
* [ ] HSI protocol scope approved.
* [ ] HSI protocol v1.0.0 released.
* [ ] MEV–EDS/SEM–EDS protocol scope approved.
* [ ] MEV–EDS/SEM–EDS protocol v1.0.0 released.
* [ ] First complete LAM+ protocol collection archived in Zenodo.

## Open decisions

* [ ] Confirm who can technically approve each protocol.
* [ ] Confirm the authoritative language used during initial drafting.
* [ ] Decide whether each system will have one comprehensive protocol or multiple linked protocols.
* [ ] Decide whether individual protocol PDFs or the complete protocol collection will be the primary Zenodo publication unit.
* [ ] Define the minimum review requirements for major and minor releases.
* [ ] Define how superseded protocols will remain accessible.
