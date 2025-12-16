# websiteBlog

This repository contains the blog content for MattyJacks.com.

## Content base path
All blog posts live under:

`content1/posts/`

## URL and routing
Target URL format:

`/blog/<year>/<slug>`

Where:
- `year` is the folder name under `content1/posts/` (4 digits)
- `slug` is the filename without `.md`

## Folder structure
Posts are organized by year:

`content1/posts/<YEAR>/<slug>.md`

Rules:
- `<YEAR>` must be 4 digits (example: `2025`)
- filenames must be kebab-case
- filenames must end with `.md`

## Post format (YAML frontmatter required)
Every post must start with YAML frontmatter.

Required fields:
- `title`
- `description`
- `date` (ISO format `YYYY-MM-DD`)
- `year` (must match the folder name)
- `slug` (must match the filename without `.md`)
- `status` (`concept`, `draft`, `hidden`, `live`, `dead`, `junk`)
- `author`

Template:
```md
---
title: "Your Post Title"
description: "One sentence description."
date: "YYYY-MM-DD"
year: "2025"
slug: "your-post-slug"
status: "concept" / "draft" / "hidden" / "live" / "dead" / "junk"
author: "Your Name"
---

## Status meanings
- `hidden`: live on site, but not linked from main blog page
- `live`: live on site and linked from main blog page
- `dead`: was once live, now is not live
- `draft`: not live yet, still a work in progress
- `concept`: same as draft but less content
- `junk`: abandoned work, decided not to continue

## Publishing rules
Only posts with:

`status: "live"`

should be shown publicly on the website.

## Images (jsDelivr)
Images can be stored inside this repo and referenced from posts using jsDelivr URLs.

jsDelivr format:

`https://cdn.jsdelivr.net/gh/<owner>/<repo>@<ref>/<path>`

Example (an image stored in this repo):

`https://cdn.jsdelivr.net/gh/mattyjacks/websiteBlog@main/content1/assets/images/random/givegigs%20512px%20logo%20v4%20a2%20glowy.png`

In Markdown:
```md
![GiveGigs logo](https://cdn.jsdelivr.net/gh/mattyjacks/websiteBlog@main/content1/assets/images/random/givegigs%20512px%20logo%20v4%20a2%20glowy.png)
```

## How to add a post
Create a new file at `content1/posts/<YEAR>/<slug>.md`.

1. Create the year folder if it does not exist: `content1/posts/<YEAR>/`.
2. Create the Markdown file: `content1/posts/<YEAR>/<slug>.md`.
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
status: "concept" / "draft" / "hidden" / "live" / "dead" / "junk"
author: "Your Name"
---
```

## Example
File path:
`content1/posts/2025/scale-facebook-ads.md`

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
