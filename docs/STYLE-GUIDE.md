# Style Guide

This guide defines the voice, tone, and formatting conventions for content
on this site. Claude references this when drafting posts and project entries.

---

## Voice and Tone

**Write like you're explaining to a smart colleague, not presenting to a committee.**

- **Direct.** Say what you mean. "I chose X because Y" not "one might consider X given Y."
- **Specific.** Concrete examples beat abstract claims. Metrics beat adjectives.
- **Honest.** Include what didn't work. "I'd do X differently" is more useful than a highlight reel.
- **Unpretentious.** No jargon without explanation. Define acronyms on first use.

### What to avoid

- Filler openers: "In today's fast-paced world..." / "It goes without saying..."
- Passive voice when active is clearer: "the system was designed" → "I designed the system"
- Hedging everything: occasional hedging is fine; constant hedging loses trust
- Clickbait titles: describe what the post actually is

---

## Formatting

### Headings

- `## H2` — major sections
- `### H3` — subsections within a section
- Avoid H4+ unless the content is genuinely complex
- Write headings as noun phrases or short questions, not full sentences

### Lists

Use **bullet lists** for unordered items, things that don't have a sequence.
Use **numbered lists** for steps, sequences, ranked items.
Keep list items parallel in grammatical structure.

### Code

Always specify the language for syntax highlighting:

````markdown
```python
def hello():
    print("hello")
```
````

For inline code, use backticks: `variable_name`, `$ command`.

For commands meant to be run in the terminal, use `bash`:

```bash
bundle exec jekyll serve
```

### Links

- Link text should describe the destination: `[Jekyll docs](url)` not `[click here](url)`
- External links open in the same tab by default (Jekyll/Markdown default)

### Images

- Always include descriptive alt text: `![Graph showing latency reduction over 3 months](image.jpg)`
- Teasers: 575×300px
- In-post images: max 800px wide (Minimal Mistakes constrains content width)
- Put post images in `assets/images/posts/YYYY-MM-DD-slug/`

---

## Blog Posts

### Titles

- Title case for blog posts
- Be descriptive, not clever — readers should know what they're getting
- Good: "How I Reduced API Latency by 40% with Response Caching"
- Avoid: "The One Weird Trick Engineers Don't Want You to Know"

### Length

- Technical posts: 800–2000 words
- Reflections: 500–1200 words
- No minimum — a tight 400-word post is better than a padded 1500-word post

### Structure

Every post should have:
1. An opening that states what the reader will learn
2. A TL;DR (even for short posts)
3. A logical flow with clear headings
4. A closing with key takeaways or next steps

---

## Project Entries

### Titles

Use the actual project name, not a description. "Neural Traffic Controller" not
"A Machine Learning Project for Traffic Optimization."

### Excerpts

One sentence. It appears in the projects grid. Make it concrete:
- Good: "Real-time traffic signal controller using reinforcement learning, deployed on FPGA."
- Avoid: "An interesting project combining machine learning and embedded systems."

### Status field

Use exactly one of: `In Progress` / `Shipped` / `Archived`

---

## Publishing Checklist

Before moving a draft to `_posts/`:

- [ ] Front matter complete (title, date, excerpt, tags)
- [ ] All `<!-- comment -->` placeholders removed
- [ ] All `[bracketed placeholder text]` filled in
- [ ] TL;DR written
- [ ] Headings are descriptive (not "Section 1")
- [ ] Code blocks have language specified
- [ ] Images have alt text
- [ ] Links tested
- [ ] `CLAUDE CONTEXT` block removed
- [ ] Read it aloud — if a sentence is hard to say, rewrite it
