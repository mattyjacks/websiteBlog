# my-blog-content

## How to add a post
Create a new file at `posts/<YEAR>/<slug>.md`.

1. Create the year folder if it does not exist: `posts/<YEAR>/`.
2. Create the Markdown file: `posts/<YEAR>/<slug>.md`.
3. Copy the frontmatter template below.
4. Keep `filename`, `slug`, and `year` consistent.

## Naming rules
- kebab-case only
- no spaces
- file extension must be `.md`
- `<YEAR>` must be 4 digits (example: `2025`)

## Frontmatter template
```md
---
title: "Your Post Title"
description: "One sentence description."
date: "YYYY-MM-DD"
year: "2025"
slug: "your-post-slug"
status: "concept" / "draft" / "live" / "dead"
author: "Your Name"
---
```

## Example
File path:
`posts/2025/scale-facebook-ads.md`

```md
---
title: "How to Scale Facebook Ads Without Nuking ROAS"
description: "A practical guide to scaling Meta ads without killing performance."
date: "2025-01-05"
year: "2025"
slug: "scale-facebook-ads"
status: "draft"
author: "Matt"
---

## The Scaling Problem
Most advertisers scale too fast...
```
