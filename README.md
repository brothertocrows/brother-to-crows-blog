# Open Blog Revolution

## What is this?

A free template for building self-hosted blogs.
It's built with [Astro](https://astro.build/).

## Who is it for?

* Writers who look for a simple solution to build self-hosted blogs.
* Developpers who look for a starter template to expand. 

## WWat do you mean by self-hosting?

An OBR Blog can be hosted anywhere. This document provides instructions to install it on the free [Netlify](https://www.netlify.com/) tier. 

## License

## Installation on Netlify

* Fork this repository (fork button on the top right corner). GitHub will create a copy of that entire project under your username. You might need to create a GitHub account.

* Create a free account on [Netlify](https://www.netlify.com/). You can login with your GitHub credentials.

* On Netlify, go to `Projects` select `Add new project/Import and existing project`

* Click on the `GitHub` icon. Select your newly created repository.

Every time you modify the blog or its contents Netlify will automatically update the website.

## Adding content

### If you want to use a writer friendly backend interface

* Open a free account on [Pages CMS](https://pagescms.org/)
* Add your OBR GitHub repository as a Project
* Open it
* Edit the `Blog Connfig`
* Add Posts and Pages

### If you're comfortable with using markdown and GitHub

* You can add posts as .mdx files in the `/src/content/posts` folder
* You can add pages as .mdx files in the `/src/pages` folder
* Media (images) must be located in `/src/content/media`
* Edit `/blog-config.yaml` to configure your blog.

Partial project structure:

```text
/
├── public/
├── src/
│   └── pages/
│   └── content/
│       └── posts/
│       └── media/
└── blog-config.yaml
```
New posts must have the following frontmatter

```yaml
---
title: Post title
description: Post description
pubDate: yyyy-mm-dd
status: published | draft
author: Author name
tags:
  - tag
cover:
  src: relative path, for example ../media/imagename
  title: string
  alt: string
---
```
Posts must have at least one tag.

`.mdx` is similar to Markdown but allows you to use HTML tags.
