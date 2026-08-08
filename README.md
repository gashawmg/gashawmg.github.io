# ChemPal Tutor Blog

Source for **[gashawmg.github.io](https://gashawmg.github.io/)** — the blog for
**[ChemPal Tutor](https://chempal.pro/)**, an AI-powered chemistry tutor with step-by-step
explanations, molecular structure rendering, practice tools, voice support, and 16-language learning.

Built with [Jekyll](https://jekyllrb.com/) and the [Minima](https://github.com/jekyll/minima)
theme, hosted on GitHub Pages.

## Structure

```
.
├── _config.yml              # site settings, theme, plugins
├── index.md                 # home page (post list)
├── about.md                 # about page
├── _posts/                  # blog posts — filenames MUST be YYYY-MM-DD-title.md
└── assets/
    ├── css/style.scss       # custom styling on top of Minima
    └── img/                 # images, including social preview cards
```

## Adding a new post

1. Create a file in `_posts/` named `YYYY-MM-DD-your-post-title.md`.
   The date prefix is required — Jekyll ignores files without it.
2. Start the file with front matter:

   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2026-08-08
   description: "One or two sentences for search results and link previews."
   categories: [chemistry, education]
   tags: [chemistry tutor, study tips]
   image: /assets/img/your-social-card.png
   ---
   ```
3. Write the body in Markdown. Add `* TOC` followed by `{:toc}` to insert an
   automatic table of contents.
4. Commit to `main` — GitHub Pages rebuilds and deploys automatically in 1–3 minutes.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## Notes

- Raw HTML (`<iframe>`, `<script type="application/ld+json">`) renders correctly on the built
  site. GitHub's own Markdown preview strips those tags — that's expected and not a problem.
- Social preview images should be 1200×630 PNG.
- `url` in `_config.yml` must stay absolute, or Open Graph images won't resolve for
  Facebook and LinkedIn.

## Links

- Live blog: <https://gashawmg.github.io/>
- ChemPal Tutor app: <https://chempal.pro/>
