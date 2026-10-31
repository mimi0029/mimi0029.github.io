# Editing Guide

All public text and images are stored in ordinary YAML, Markdown, or image files.
You do not need to edit Hugo templates.

## Replace the profile image

Replace:

```text
static/media/yi-ma-home.jpg
```

Keep the same file name. The homepage displays this image at its original 3:2
aspect ratio without cropping. If a future replacement uses a different aspect
ratio, update the `aspect-ratio` value in
`layouts/_partials/hooks/head-end/portfolio-photo.html`.

## Edit biography, education, experience, skills, or awards

Open:

```text
data/authors/me.yaml
```

Preserve the indentation and update only the text between the field names.

## Add a project

Copy an existing folder under `content/projects/`, rename the folder, and edit
its `index.md`. Put an optional project image named `featured.jpg` or
`featured.png` in the same folder.

For a portfolio-style case study, use these headings:

```markdown
## Technical problem

## My contribution

## Methods

## Evidence and outcomes
```

Set `featured: true` in the front matter when the project should appear in the
three-card homepage selection.

## Add a publication

Copy an existing folder under `content/publications/`, rename the folder, and
edit its `index.md`. Unknown DOI, URL, volume, or issue fields should be omitted
rather than guessed.

## Create a document page

Create:

```text
content/research-statement/index.md
```

Example:

```markdown
---
title: "Research Statement"
summary: "My research agenda in integrated PV–storage and energy management."
date: 2026-10-19
---

## Research focus

Write the document here in Markdown.
```

Add the page to `config/_default/menus.yaml`:

```yaml
  - name: Research Statement
    url: research-statement/
    weight: 55
```

Images may be stored beside the document and linked with:

```markdown
![Figure description](figure-1.png)
```

Downloadable files belong in `static/uploads/` and can be linked with:

```markdown
[Download the document](../uploads/file.pdf)
```

## Replace the downloadable CV

The current editable English CV is:

```text
static/uploads/Yi_Ma_CV_editable.docx
```

Replace it with the same file name to keep the homepage link working. When the
final PDF is ready, save it as `static/uploads/Yi_Ma_CV.pdf` and change the link
in `content/_index.md` from `Yi_Ma_CV_editable.docx` to `Yi_Ma_CV.pdf`.
