# LAM+ protocol templates

[English](README.md) | [Português](README.pt-BR.md)

These files provide the minimum shared structure for LAM+ laboratory protocols. They are content templates, not completed procedures.

## Create a protocol

1. Copy both language templates into the relevant equipment `protocols/` directory.
2. Give both files the same base name:

```text
acquisition.md
acquisition.pt-BR.md
```

3. Replace `LAM-XXX-000` only after the protocol scope and identifier are confirmed.
4. Keep the protocol ID, version, date, authors, reviewers and status synchronized across languages.
5. Replace or remove every instructional HTML comment before approval. Comments do not appear in normal Markdown rendering or Pandoc output.
6. Remove optional sections only when they do not apply; do not leave unexplained empty sections.

## Images

From a protocol inside `equipment/<system>/protocols/`, reference shared images with relative paths:

```markdown
![Descriptive caption.](../assets/common/image-name.png){#fig-image-name width=85%}
```

Use:

- `assets/common/` for photographs and figures usable in both languages;
- `assets/en/` for graphics containing English text;
- `assets/pt-BR/` for graphics containing Portuguese text.

Use lowercase hyphen-separated filenames and record source and licensing in `assets/IMAGE_CREDITS.md`.

## PDF generation

When the repository Pandoc defaults are configured, run from the repository root:

```bash
pandoc --defaults templates/defaults-en.yaml \
  equipment/<system>/protocols/protocol-name.md \
  -o protocol-name-en.pdf
```

```bash
pandoc --defaults templates/defaults-pt-BR.yaml \
  equipment/<system>/protocols/protocol-name.pt-BR.md \
  -o protocol-name-pt-BR.pdf
```

Generated PDFs are release artifacts and should not normally be committed with the Markdown sources.

## Approval

Only protocols explicitly marked `Approved` are authorized LAM+ procedures. Technical, safety and bilingual review must be completed before changing the status.

