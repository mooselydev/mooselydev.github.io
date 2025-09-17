---
title: Blog Setup
pubDatetime: 2025-09-17T12:13:00+00:00
tags:
  - blogging
description: Blog setup and quick-reference post notes.
---

# Blog Setup

Initial blog setup instructions can be found [here](https://astro-paper-i18n.netlify.app/posts/how-to-configure-astropaper-theme/).

# Making a Post

To make a post, create a markdown file within `paper/src/data/blog/<your-markdown-file-here>.md`.

Posts need a bit of frontmatter to function properly, at the minimumum the following is required:
```
---
title: Blog Setup
description: Blog setup and quick-reference post notes.
pubDatetime: 2025-09-17T12:13:00+00:00
tags:
  - blogging
---
```

While `tags` are not *technically* required, tagging posts is a great way to find relevant posts for given topics. More information about adding posts can be found in the upstream [documentation](https://astro-paper-i18n.netlify.app/posts/adding-new-posts-in-astropaper-theme/)

# Hosting

