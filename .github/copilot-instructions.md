# GitHub Copilot Instructions

## Static assets (images)

This site is deployed to GitHub Pages at `/ai-for-coding/` (not root). All references to static assets must include the subpath:

```markdown
![alt text](/ai-for-coding/images/filename.jpg)
```

**Not** `/images/filename.jpg` — that resolves to the GitHub Pages root and will 404.

Images go in `static/images/` and must include source attribution beneath:

```markdown
![Description](/ai-for-coding/images/example.jpg)
*Source: [Author, Title](https://example.com/source)*
```

## Git commits

Use `--no-gpg-sign` for all commits (SSH signing requires passphrase).
