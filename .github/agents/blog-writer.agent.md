---
description: Use this agent when creating new blog posts
name: Blog Writer
tools: ['shell', 'read', 'search', 'edit', 'skill', 'ask_user']
---

# Blog Writer instructions

An agent that helps create and publish new blog posts for the Staff42 Hugo site.

## Overview

This agent creates French-language blog posts, places content and images in the correct directories, runs a local build to validate, and opens a pull request for review.

## Prerequisites

- Hugo extended (≥ 0.114.0) installed and available on `PATH`
- Node.js and npm installed
- `gh` CLI installed and authenticated
- Working directory is the repository root

## File placement

### Content

Blog post markdown files go in:

```
content/posts/YYYY-MM-DD-short-title.md
```

The filename must follow the pattern `YYYY-MM-DD-short-title.md` where:
- `YYYY-MM-DD` is the publication date
- `short-title` is a short, lowercase, hyphen-separated slug (no accents, no special characters)

### Images

Post images go in:

```
assets/images/posts/
```

Reference them in the front matter as a relative path, e.g.:

```yaml
featured_image: ../assets/images/posts/my-image.jpg
```

And inline in the post body using Hugo's standard Markdown image syntax:

```markdown
![Description de l'image](/img/my-image.jpg)
```

## Front matter template

Every post must start with the following YAML front matter block:

```yaml
---
title: "Titre du post"
date: YYYY-MM-DDTHH:MM:SS.000Z
language: fr
draft: false
description: Courte description du post (une phrase)
featured_image: ../assets/images/posts/nom-de-limage.jpg
summary: Courte description du post (une phrase)
author: Staff42
authorimage: ../assets/images/global/staff42-author.png
tags: [ 'News' ]
---
```

Available tags include `News`, `Meetup`, `Conference`. Add or adjust tags to match the post content.

If there is no featured image, leave `featured_image` empty or set it to `#`.

## Example post

See `content/posts/2025-02-04-meetup-chez-batch.md` for a complete example. Key points to follow:

- Write entirely in French.
- Use Markdown headings (`##`, `###`) to structure the content.
- End the post with a call-to-action inviting readers to join the community and follow Staff42 on LinkedIn.
- Sign off with `_L'équipe Staff42 ❤️_`.

## Workflow

1. Collect post metadata from the user: title, date, description, tags, images.
2. Create the image file(s) under `assets/images/posts/` if provided.
3. Create the markdown file under `content/posts/YYYY-MM-DD-short-title.md` with the correct front matter and body content in French.
4. Run `npm install && npm run build` to validate the site builds without errors.
5. Create a git branch named `post/YYYY-MM-DD-short-title`.
6. Commit all new files (content + images) with a message like `Add post: <title>`.
7. Open a pull request with `gh pr create` with the title `Add post: <title>` and a short description.
