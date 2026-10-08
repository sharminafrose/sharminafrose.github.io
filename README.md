# sharminafrose.github.io

Personal website of Sharmin Afrose, built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll) and deployed to GitHub Pages at <https://sharminafrose.github.io>.

## Where content lives

| Content | File |
| --- | --- |
| About page bio and photo | `_pages/about.md`, `assets/img/prof_pic.jpg` (currently a placeholder) |
| Papers and presentations | `_bibliography/papers.bib`, `presentations.bib` |
| CV page (web) | `_data/cv.yml` |
| CV PDF | `assets/pdf/AfroseS_CV.pdf` |
| Software releases | `_data/software.yml` |
| Awards | `_data/awards.yml` |
| Mentoring and volunteer work | `_data/service.yml` |
| Social links and email | `_data/socials.yml` |
| Theme color and small style tweaks | `_sass/_custom.scss` |

## Common updates

**Add a paper.** Append a BibTeX entry to `_bibliography/papers.bib`. Use `doi={...}` for a DOI button and `pdf={file.pdf}` to link `assets/pdf/file.pdf`.

**Citation counts.** `.github/workflows/update-citations.yml` refreshes `_data/citations.yml` from Google Scholar (ID in `_data/socials.yml`) and redeploys.

**Local preview.** `bundle install && bundle exec jekyll serve`.
