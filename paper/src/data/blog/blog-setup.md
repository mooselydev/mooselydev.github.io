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

I setup initial hosting on GitHub pages. The documentation starts [here](https://docs.github.com/en/pages)

For GitHub to host an AstroJS backed blog, it must know the content that needs to be hosted. This can be in the form of files directly in the repository, or as an output of a GitHub Action. In the case of Astro, it needs to be the output of a GitHub action as the builder needs to produce the appropriate output content. There are additional details on the Astro documentation site [here](https://docs.astro.build/en/guides/deploy/github/)

# Custom Domain

When configuring a custom domain for a GitHub site GitHub suggests to configure the GitHub Pages settings before the adding the DNS records to your DNS provider. This ensures your domain will not get hijacked by someone else on a GitHub page. Information about that [here](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#about-custom-domain-configuration).

The AstroJS docs instruct to add a CNAME file to your project. But there is a note in the GitHub [docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain) that states:
> you are publishing from a custom GitHub Actions workflow, no CNAME file is created, and any existing CNAME file is ignored and is not required.

For non-apex domains (aka subdomains) GitHub [prefers](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#dns-records-for-your-custom-domain) you use CNAME records.

