# Hashed Science

**Live site: <https://sci-coder.github.io/shshaw_blog/>**

Personal site of **Syed Hashim Shah**: picture-first articles with animations on quantitative ML,
generative AI for finance, physics-based machine learning and optimization.

- LinkedIn: <https://www.linkedin.com/in/syed-hashim-shah/>
- GitHub: <https://github.com/sci-coder>
- CV: <https://sci-coder.github.io/shshaw_blog/about/cv/>

## How it is built

- [Hugo](https://gohugo.io/) (extended, v0.146) with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
  theme (git submodule in `themes/`).
- KaTeX math on pages with `math: true` (`layouts/partials/extend_head.html`).
- Every push to `master` builds and deploys to GitHub Pages (`.github/workflows/hugo.yaml`).

## Writing a post

Each article is a page bundle: `content/posts/<slug>/index.md` plus its GIFs. Start with
`draft: true`, preview locally, and set `draft: false` when it is ready.

```bash
hugo server -D        # preview at http://localhost:1313/shshaw_blog/ (drafts included)
hugo --minify         # production build into public/
```

## SEO

- `sitemap.xml`, `robots.txt` and an RSS feed (`index.xml`) are generated on every build.
- Site description, keywords, author schema and a default share image
  (`static/images/og-default.png`, 1200x630) are set in `config.yaml`.
- Give each post a `title`, a one-sentence `summary` or `description`, `tags`, and a `cover`
  image; these feed search results and link previews.
- To verify the site in Google Search Console or Bing, paste the code into
  `params.analytics.*.SiteVerificationTag` in `config.yaml`, then submit `sitemap.xml`.
