# Yi Ma · Academic CV Website

This repository contains an editable HugoBlox Academic CV website for Yi Ma.
It is currently prepared and tested locally; publication is intentionally deferred.

## Where to edit

- Personal profile, education, experience, skills, languages, and awards:
  `data/authors/me.yaml`
- Homepage structure and introductory text:
  `content/_index.md`
- Navigation:
  `config/_default/menus.yaml`
- Site identity, colors, typography, and behavior:
  `config/_default/params.yaml`
- Projects:
  `content/projects/<project-name>/index.md`
- Publications:
  `content/publications/<publication-name>/index.md`
- Profile image:
  `static/media/yi-ma-home.jpg`
- Downloadable editable CV:
  `static/uploads/Yi_Ma_CV_editable.docx`

The homepage follows five portfolio sections: About, Selected Projects,
Technical Skills, Publications & Patents, and CV & Contact. Detailed education,
experience, awards, and language data remain available as editable CV content
in `data/authors/me.yaml` and `content/experience.md`.

See `EDITING_GUIDE.md` for copy-and-paste examples.

## Local preview

The project requires Hugo Extended, Go, Node.js, and the packages listed in
`package.json`. Run:

```powershell
hugo server --disableFastRender
```

Then open the local URL printed by Hugo.

## Publication

The included GitHub Actions workflow can build and publish this project through
GitHub Pages after the repository owner enables Pages. No deployment has been
performed as part of the local migration.

## Public-information boundary

The website intentionally excludes phone number, birth date, hometown,
political affiliation, detailed grades, and private social-media identifiers.
