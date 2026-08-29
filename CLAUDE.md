# Ullas Landing Page

## No-indexing requirement (MANDATORY)

This website must NOT be indexed by search engines. When creating or editing
ANY HTML page in this repository, always include this tag inside `<head>`,
as early as possible:

```html
<meta name="robots" content="noindex, nofollow, noarchive">
```

Supporting configuration already in place — do not remove or weaken it:

- `vercel.json` sends an `X-Robots-Tag: noindex, nofollow, noarchive` header
  on every response (applies when hosted on Vercel).
- `robots.txt` deliberately ALLOWS crawling. Do not add `Disallow: /` —
  crawlers must be able to fetch pages to see the noindex directive;
  blocking them can leave URLs indexed via external links.

Also: do not add a sitemap, sitemap reference, or canonical/Open Graph tags
that invite indexing, and do not submit the site to any search console.
