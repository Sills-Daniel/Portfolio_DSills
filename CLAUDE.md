# Portfolio — Claude Project Instructions

> Entry point for every Claude Code session in this repo.
> Read this file first, then follow the Session Startup Checklist.

---

## About This Project

Personal portfolio and blog for **Daniel Sills** — R&D Engineer, ECE MS
graduate (University of Louisville), and published researcher in advanced
manufacturing and AI-driven process optimization. Hosted on GitHub Pages.

**Stack:** Jekyll · Minimal Mistakes theme (dark skin) · Markdown content
**Repo:** `Sills-Daniel/Portfolio-DSills` (public)

**Experience level:** Daniel is comfortable with Markdown but has limited
HTML experience and no prior Jekyll/static-site-generator experience.
- Explain new concepts in plain terms with a concrete example
- Prefer showing the minimal change needed over a full rewrite
- When touching SCSS, explain what the rule does and where it applies

---

## Session Startup Checklist

Run through this before touching any files:

1. **`_brainstorm/sessions/`** — read the most recent dated file for prior
   session context, open questions, and what to do first
2. **`_brainstorm/site-roadmap.md`** — current phase and next priorities
3. **`_brainstorm/ideas-inbox.md`** — any new ideas captured since last session

> `_brainstorm/` is **gitignored** (local-only, never pushed). If it's
> missing, the repo was freshly cloned — rebuild context from `git log`
> and this file, then ask Daniel for his latest session notes.

---

## Build Commands

```bash
bundle install                          # First-time setup (installs gems)
bundle exec jekyll serve --drafts       # Local preview → http://localhost:4000
bundle exec jekyll serve                # Preview published content only
bundle exec jekyll build                # Production build → _site/
```

**Troubleshooting:**
- `Liquid Exception` → usually a syntax error in front matter YAML or a
  missing layout name; check the file Jekyll is complaining about
- `Cannot find theme` → run `bundle install` again; remote theme may not
  be cached yet
- SCSS errors → check import order in `assets/css/main.scss` (variables
  before skin before theme before overrides)

---

## Directory Map

```
_config.yml      Site config: title, author, theme skin, plugins, collections
Gemfile          Ruby dependencies — pins github-pages gem for build parity
CNAME            Domain placeholder — update when domain is purchased
index.md         Homepage (layout: home — shows recent posts)
about.md         About page — filled with Daniel's bio and background
projects.md      Projects collection listing (layout: collection, grid view)
404.md           Custom not-found page

_posts/          Published blog posts — filename MUST be YYYY-MM-DD-slug.md
_drafts/         Unpublished posts — no date prefix; visible with --drafts flag
_projects/       Project showcase entries — one .md file per project
_templates/      Fill-in outlines — COPY to _drafts/ or _projects/, never edit

_data/
  navigation.yml Nav menu items (About, Blog, Projects, Resume)

assets/
  css/main.scss  SCSS entry point — controls import order (see SCSS section)
  js/main.js     Custom JavaScript — loaded after Minimal Mistakes scripts
  images/
    profile/     avatar.jpg — headshot shown in author sidebar
    posts/       Organized by post slug: YYYY-MM-DD-slug/image.jpg
    projects/    Organized by project slug: slug/teaser.jpg
    site/        Favicon, logo, site chrome
  docs/
    resume.pdf   Resume — linked from nav and optionally from about.md
  fonts/         Custom web fonts (currently unused)
  videos/        Small clips only — prefer YouTube/Vimeo embeds

_sass/
  custom/
    _variables.scss  Pre-import variable overrides (all commented; uncomment to apply)
    _overrides.scss  Post-import CSS rule overrides

docs/            Human-facing docs — excluded from Jekyll build output
  CONTENT-WORKFLOW.md  Full template → draft → publish pipeline
  STYLE-GUIDE.md       Voice, tone, formatting, publishing checklist
  DEPLOY.md            (planned) deployment and domain notes

_brainstorm/     LOCAL ONLY (gitignored) — ideation and session handoffs
  ideas-inbox.md       Rapid capture
  blog-ideas.md        Blog post topic queue
  project-ideas.md     Project backlog + published works copyright tracker
  site-roadmap.md      Phase tracking and long-term vision
  decisions/           ADR-lite: dated records of non-trivial decisions
  sessions/            Per-session handoff notes (TEMPLATE.md + dated files)
```

---

## Content Workflow

### New blog post
```bash
cp _templates/blog-post-outline.md _drafts/my-slug.md
# edit _drafts/my-slug.md
# when ready to publish:
mv _drafts/my-slug.md _posts/YYYY-MM-DD-my-slug.md
```

Template variants: `blog-post-outline.md` (general) ·
`blog-post-technical.md` (tutorials) · `blog-post-reflection.md`
(lessons learned)

### New project
```bash
cp _templates/project-outline.md _projects/my-slug.md
# for a longer write-up:
cp _templates/project-case-study.md _projects/my-slug.md
```

### New idea
One line in `_brainstorm/ideas-inbox.md`. Organize into
`blog-ideas.md` or `project-ideas.md` when ready.

Full details: `docs/CONTENT-WORKFLOW.md`

---

## SCSS Customization

The SCSS system has three files with a strict import order:

```
assets/css/main.scss          ← controls the order; do not reorder imports
_sass/custom/_variables.scss  ← variable overrides (before theme import)
_sass/custom/_overrides.scss  ← CSS rule overrides (after theme import)
```

**To change a color or font:** uncomment and edit the relevant line in
`_sass/custom/_variables.scss`. All Minimal Mistakes variables use
`!default`, so pre-defining them here wins.

**To add a CSS rule:** add it to `_sass/custom/_overrides.scss`.
Use browser DevTools to find the exact class name to target.

**Available dark skin variables** (approximations — inspect the theme source
for exact values):
- Background: `#1a1a1a` · Text: `#eaeaea` · Border: `#3d3d3d`
- Inspect `https://github.com/mmistakes/minimal-mistakes` `_sass/` for full list

---

## Theme

- **Minimal Mistakes** loaded via `jekyll-remote-theme`
- Skin: `minimal_mistakes_skin: "dark"` in `_config.yml`
- Other skin options: `air` · `aqua` · `contrast` · `default` · `dirt` ·
  `mint` · `neon` · `plum` · `sunrise`
- Layouts in use: `home` (index) · `single` (posts, pages, projects) ·
  `collection` (projects listing)

---

## Domain

No custom domain yet. When purchased:
1. Replace the comment in `CNAME` with the bare domain (e.g. `danielsills.com`)
2. Set `url: "https://danielsills.com"` in `_config.yml`
3. Configure DNS at your registrar per GitHub Pages docs

---

## Implementation Phases

| Phase | Status | Description |
|-------|--------|-------------|
| 1 | **Complete** | Skeleton: config, theme, homepage, brainstorm scaffold |
| 2 | **Complete** | Pages, nav, templates, sample draft/project, workflow docs |
| 3 | **Complete** | Assets structure, SCSS layer, resume, profile photo |
| 4 | **Complete** | Claude workflow polish: ADRs, refined CLAUDE.md |

---

## Gotchas & Lessons Learned

- **`_posts/` filename is strict.** Jekyll silently ignores posts without
  the `YYYY-MM-DD-` prefix. Always rename when moving from `_drafts/`.
- **SCSS import order matters.** Variables must be imported before the skin;
  custom rule overrides must come after. Reordering breaks the cascade.
- **`docs/` is excluded from the build.** It's in `_config.yml`'s `exclude`
  list intentionally — content there is for humans/Claude, not site visitors.
- **`_brainstorm/` is gitignored.** Changes there never appear in `git status`.
  Write session notes before ending a session or they're gone on clone.
- **Remote theme SCSS.** With `jekyll-remote-theme`, you cannot override
  theme files directly — use `_sass/custom/` and the import chain instead.
- **LinkedIn URL needs `https://`.** Bare `www.` URLs break the author
  sidebar link. Always prefix external URLs with the protocol.
- **`projects.md` uses `layout: collection`.** Adding projects is just
  creating a new `.md` in `_projects/` — no other wiring needed.
- **Teaser images are 575×300px.** Other sizes work but may crop
  unexpectedly in the projects grid. Stick to that ratio.

---

## End-of-Session Protocol

Before ending any session, write a handoff note:

```
_brainstorm/sessions/YYYY-MM-DD-topic.md
```

Use the template at `_brainstorm/sessions/TEMPLATE.md`. Sections:
What We Did · Decisions Made · Open Questions · Files Changed ·
Next Session Should · Current Phase

Also update `_brainstorm/site-roadmap.md` if the phase or priorities changed.

---

## Rules

- Draft in `_drafts/` before publishing to `_posts/`
- Post images → `assets/images/posts/YYYY-MM-DD-slug/`
- Project images → `assets/images/projects/slug/`
- Teasers should be 575×300px (or same aspect ratio)
- Check copyright before committing published works →
  `_brainstorm/decisions/copyright-review.md`
- Follow voice and tone → `docs/STYLE-GUIDE.md`
- SCSS changes → `_sass/custom/` only; do not create `_sass/minimal-mistakes/`
- External URLs in `_config.yml` and Markdown must include `https://`
- This file extends global rules at `~/.claude/rules/common/` —
  project-specific rules take precedence where they conflict
