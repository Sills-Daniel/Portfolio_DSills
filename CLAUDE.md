# Portfolio — Claude Project Instructions

> This file is the entry point for every Claude Code session in this repo.
> Read it first. Then follow the Session Startup Checklist below.

## What This Repo Is

Personal portfolio and blog for Daniel Sills, hosted on GitHub Pages.
Stack: Jekyll + Minimal Mistakes theme (dark skin) + Markdown content.

Daniel has limited HTML experience and no prior experience with Jekyll or
static site generators. Explain concepts in plain terms; avoid assuming
framework familiarity. When introducing a new concept, show a minimal
concrete example alongside any abstraction.

## Session Startup Checklist

Run through this at the start of every session before touching any files:

1. Read `_brainstorm/sessions/` — open the **most recent dated file** for
   prior session context and open questions.
2. Read `_brainstorm/site-roadmap.md` — check current phase and next
   priorities.
3. Skim `_brainstorm/ideas-inbox.md` — pick up any ideas captured since
   the last session.

> `_brainstorm/` is gitignored (local-only). If these files are missing,
> the repo was freshly cloned on a new machine — ask Daniel to share his
> brainstorm notes, or start the session by rebuilding context from git log
> and this file.

## Build Commands

```bash
bundle install                         # First-time setup
bundle exec jekyll serve --drafts      # Local preview → http://localhost:4000
bundle exec jekyll build               # Production build → _site/
```

## Directory Map

```
_posts/          Published blog posts (YYYY-MM-DD-slug.md required)
_drafts/         Unpublished drafts (no date prefix needed)
_projects/       Project showcase collection
_templates/      Fill-in outlines — COPY, never edit in place
_layouts/        Jekyll HTML templates (Phase 2+)
_includes/       Reusable HTML partials (Phase 2+)
assets/          CSS, JS, images, docs (Phase 3+)
docs/            Human-facing workflow docs (Phase 2+)
_brainstorm/     LOCAL ONLY (gitignored) — ideation and session notes
CNAME            Domain placeholder — update when domain is purchased
```

## Content Workflow (short version)

- **New blog post**: copy `_templates/blog-post-outline.md` → save as
  `_drafts/slug.md` → fill in → move to `_posts/YYYY-MM-DD-slug.md`
- **New project**: copy `_templates/project-outline.md` → save as
  `_projects/slug.md` → fill in
- **New idea**: one line in `_brainstorm/ideas-inbox.md`

Full workflow: `docs/CONTENT-WORKFLOW.md` (created in Phase 2).

## Theme

- **Minimal Mistakes** remote theme, dark skin
- Skin is set by `minimal_mistakes_skin: "dark"` in `_config.yml`
- To change skin options: air, aqua, contrast, dark, default, dirt,
  mint, neon, plum, sunrise

## Domain

No custom domain yet. When purchased:
1. Add the domain to `CNAME` (replace the placeholder comment)
2. Set `url: "https://yourdomain.com"` in `_config.yml`
3. Configure DNS at your registrar (GitHub Pages docs cover this)

## Implementation Phases

| Phase | Status | Description |
|-------|--------|-------------|
| 1 | **Complete** | Skeleton: config, theme, homepage, brainstorm scaffold |
| 2 | **Complete** | Pages, nav, templates, sample draft/project, workflow docs |
| 3 | Not started | Assets, SCSS, resume, published works |
| 4 | Not started | Claude workflow polish: ADRs, session template refinement |

## End-of-Session Protocol

Before ending any session, write a handoff note to
`_brainstorm/sessions/YYYY-MM-DD-topic.md` using the template at
`_brainstorm/sessions/TEMPLATE.md`. Update `_brainstorm/site-roadmap.md`
if the current phase or priorities changed.

## Rules

- Always draft in `_drafts/` before publishing to `_posts/`
- Images for a post: `assets/images/posts/YYYY-MM-DD-slug/`
- Images for a project: `assets/images/projects/slug/`
- Check copyright before committing any published works —
  see `_brainstorm/decisions/` for the running review log
- Follow voice and tone in `docs/STYLE-GUIDE.md` (Phase 2+)
- This file extends global rules at `~/.claude/rules/common/` —
  project-specific rules here take precedence where they conflict
