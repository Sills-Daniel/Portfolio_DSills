# Daniel Sills — Personal Portfolio

Personal portfolio and blog hosted on GitHub Pages, built with [Jekyll](https://jekyllrb.com/) and the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme.

## Local Development

**Prerequisites:** Ruby 3.x, Bundler

```bash
bundle install                              # Install dependencies (first run only)
bundle exec jekyll serve --drafts           # Preview at http://localhost:4000
bundle exec jekyll build                    # Build to _site/
```

## Content

| Directory | Purpose |
|-----------|---------|
| `_posts/` | Published blog posts (`YYYY-MM-DD-slug.md`) |
| `_drafts/` | Unpublished drafts (rendered with `--drafts` flag) |
| `_projects/` | Project showcase entries |
| `_templates/` | Outline templates — copy these to start new content |
| `assets/` | Images, CSS, JS, documents |
| `docs/` | Workflow and style documentation |

## License

Code: [MIT](LICENSE) · Content: © Daniel Sills, all rights reserved unless noted otherwise.
