# Build a website with Quarto and GitHub Pages

Training materials for a short (about 2.5 hour) workshop that teaches
participants how to build and publish a website using
[Quarto](https://quarto.org/) and [GitHub Pages](https://pages.github.com/),
working entirely in the web browser.

## Overview

Participants sign up to GitHub, create a repository that publishes to GitHub
Pages, add content to a Quarto website, create a navbar and change the look of the
site with `styles.css`. Nothing is installed on participants' computers. Quarto
is run by a GitHub Actions workflow each time a change is committed.

## Audience

Researchers, research support staff and others who want a simple website and
to be able to update it easily. No experience of GitHub, Quarto, HTML or
programming is assumed.

## Learning objectives

Participants will learn how to:

- Set up a GitHub account using a Google account, a Microsoft email address or any other email address
- Create and configure a repository to publish to GitHub Pages
- Use Quarto to create website content (`.qmd` files)
- Create a navbar
- Use `styles.css` to change the look of the website

## Repository structure

```
├── index.qmd            # Welcome page and workshop overview
├── before.qmd           # Pre-course instructions
├── materials.qmd        # Workshop materials and exercises
├── _quarto.yml          # Quarto project configuration
├── _brand.yml           # Brand colours and fonts
├── styles.css           # Custom CSS styling
├── images/              # Logo and other images (copy from the quarto-intro template)
├── .github/workflows/   # GitHub Actions workflow that builds and deploys the site
└── CITATION.cff       # Citation metadata
```

## Instructor notes

- **Pages needs a public repository** on a free GitHub account. Tell
  participants this when they create their repository.
- **Account sign-up.** GitHub's help pages list Google and Apple as the
  supported "continue with" providers, not Microsoft, so Microsoft users sign up with the
  email form using their Microsoft address (Part 1, Option 2). Sign-up screens
  change, so do a dry run with a fresh account in the days before the workshop
  and update the screenshots or wording if they differ.
- **Email codes.** Participants must be able to open the inbox they sign up
  with. Organisation addresses sometimes delay or block the verification email,
  so have participants start Part 1 early in the session.
- **Managed computers.** Check that `github.com` and `github.io` are not blocked on
  computers provided by organisations.
- **Waiting for builds.** Each commit takes a minute or two to appear on the
  website. Use the wait for a short explanation of what is happening, and
  encourage participants to make several changes per commit.
- **Pace.** The challenges are optional and can be dropped to fit a two hour
  slot, or used to stretch to three hours. Parts 1 and 2 are where most people
  need help (accounts, indentation in the workflow).
- **Workflow versions.** `.github/workflows/publish.yml` uses
  `actions/checkout@v4`, `quarto-dev/quarto-actions/setup@v2`,
  `actions/configure-pages@v5`, `actions/upload-pages-artifact@v3` and
  `actions/deploy-pages@v4`. Check that these are still current
  before each run of the course, and test the full workflow on a throwaway
  repository.
- **Building locally.** If you would like to preview this site yourself, install
  [Quarto](https://quarto.org/docs/get-started/) and run `quarto preview`.

## Licence

These materials are licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — you are free to share and adapt them for non-commercial purposes, provided you give appropriate credit and distribute any adaptations under the same licence.