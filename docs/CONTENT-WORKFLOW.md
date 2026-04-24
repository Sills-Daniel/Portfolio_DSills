# Content Workflow

## The Pipeline

```
_templates/  →  _drafts/  →  _posts/  or  _projects/
(outline)       (writing)    (published)
```

---

## Blog Posts

### 1. Start a draft

Pick the right template from `_templates/`:

| Template | Use when |
|----------|---------|
| `blog-post-outline.md` | General post — most common |
| `blog-post-technical.md` | Tutorial, how-to, implementation write-up |
| `blog-post-reflection.md` | Lesson learned, retrospective, personal essay |

Copy it to `_drafts/`:

```bash
cp _templates/blog-post-outline.md _drafts/my-post-slug.md
```

No date prefix needed in `_drafts/`.

### 2. Fill in the front matter

At minimum, set:
- `title` — the post title
- `date` — today's date (`YYYY-MM-DD`)
- `excerpt` — 1-2 sentences for listing pages and SEO
- `tags` — 2-5 lowercase tags

### 3. Write

Preview locally with:

```bash
bundle exec jekyll serve --drafts
```

Drafts appear at `http://localhost:4000` alongside published posts.

### 4. Publish

When the post is ready, move it to `_posts/` with the date prefix:

```bash
mv _drafts/my-post-slug.md _posts/2026-04-24-my-post-slug.md
```

**Required filename format:** `YYYY-MM-DD-slug.md`
Jekyll will not build a post without the date prefix.

### 5. Add images

Put post images in:

```
assets/images/posts/YYYY-MM-DD-slug/
```

Reference them in the post as:

```markdown
![Alt text](/assets/images/posts/2026-04-24-my-post/image.jpg)
```

---

## Projects

### 1. Start a project entry

```bash
cp _templates/project-outline.md _projects/my-project.md
# For a longer write-up:
cp _templates/project-case-study.md _projects/my-project.md
```

No date prefix needed. The `date` field in the front matter controls sort order.

### 2. Fill in the front matter

At minimum:
- `title`
- `excerpt` — shown in the projects grid
- `date`
- `sidebar.text` for Status, Stack, Links

### 3. Add project images

```
assets/images/projects/my-project/
```

The `header.teaser` image shows in the projects grid (575×300px recommended).

### 4. Published works

Before committing any externally published work (papers, reports, articles):
1. Check `_brainstorm/decisions/copyright-review.md`
2. Find the publisher's self-archiving policy (SHERPA/RoMEO is useful)
3. Update the review log with your finding before adding the file

---

## Asking Claude to Draft Content

To ask Claude to write or outline a post or project:

1. Drop your notes/outline into `_brainstorm/ideas-inbox.md` or directly into a `_drafts/` file
2. Tell Claude which template to use and what the post is about
3. Claude will fill in the template and flag placeholders you need to personalize
4. Review and edit before publishing — Claude drafts are starting points, not final copy

---

## Quick Reference

| Action | Command |
|--------|---------|
| Local preview (with drafts) | `bundle exec jekyll serve --drafts` |
| Local preview (published only) | `bundle exec jekyll serve` |
| Build for production | `bundle exec jekyll build` |
| New blog draft | `cp _templates/blog-post-outline.md _drafts/slug.md` |
| New project | `cp _templates/project-outline.md _projects/slug.md` |
| Publish a draft | `mv _drafts/slug.md _posts/YYYY-MM-DD-slug.md` |
