# Notes for Claude

## About this repo
Personal academic website (al-folio Jekyll theme) for Licheng Liu, hosted at lichengliu03.github.io.

## User preferences

- **Don't fabricate dates or facts.** If the source (e.g. CV PDF) doesn't give a specific date for an event, don't invent one. Either ask, or skip adding the item. Same goes for any other detail not in the source.
- **Don't include "in submission" / "under review" papers** in `_bibliography/papers.bib`. Only list accepted publications, preprints with a public link, or accepted workshop papers.
- **Don't expose the CV page or PDF on the site** unless explicitly asked. Keep `_pages/cv.md` with `nav: false` and no `cv_pdf` set.
- **Prefer minimal, conservative edits.** When updating from a source document, prefer fewer additions over speculative ones. Ask before adding content I can't verify from the source.
- The user communicates in Chinese; replies in Chinese are welcome.

## Repo conventions
- News items live in `_news/` as individual markdown files with `date:` front matter — they render on the homepage in reverse-chronological order.
- Publications are driven by `_bibliography/papers.bib`; `selected={true}` controls what shows on the homepage.
- Bio lives in `_pages/about.md`.
