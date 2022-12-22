---
title: Migrating from Hugo
description: Tips for migrating an existing Hugo project to Astro
layout: ~/layouts/MigrationLayout.astro
stub: true
framework: Hugo
---

[Hugo](https://gohugo.io) is an open-source static site generator built on Go.

## Key Similarities between Hugo and Astro

Hugo and Astro share some similarities that will help you migrate your project:

- Hugo and Astro are both modern static-site generators, ideally suited to content-focused sites like blogs.

- Hugo and Astro both allow you to author your content in Markdown. However, Hugo allows you to write frontmatter in YAML, TOML or JSON and recognizes several special properties while allowing for custom properties. Astro recognizes YAML frontmatter, but has very few special frontmatter properties. Almost all of your frontmatter will be user-defined. Although many of your existing Hugo frontmatter properties will not be "special" in Astro, this meta data can be accessed and used by Astro components.

- Hugo and Astro both allow you to enhance your site with a variety of plugins and external packages.



## Key Differences between Hugo and Astro

When you rebuild your Hugo site in Astro, you will notice some important differences:

- Hugo uses Go for page templating. Astro syntax is a JSX-like superset of HTML.

- Hugo sites are created using Markdown (`.md`) files for page content and HTML (`.html`) templates for layout. Astro is component-based, and uses Astro components, which include HTML templating for pages, layouts and individual UI elements. Astro can also create pages from `.md` and `.mdx` files, using an Astro layout component for wrapping Markdown content in a page template.

- While Hugo can use "partials" for reusable layout elements, Astro is entirely component-based. Any `.astro` file can be a component, a layout or an entire page, and can import and render any other Astro components. Astro components can also render other UI framework components (e.g. React, Svelte, Vue, Solid) as well as content or meta data from other files in your project, such as Markdown or MDX.

## Switch from Hugo to Astro

To convert a Hugo blog to Astro, start with our blog theme starter template, or explore more community blog themes in our [theme showcase](https://astro.build/themes). Bring your existing Markdown (or MDX, with our optional integration) files as content to [create Markdown or MDX pages](/en/guides/markdown-content/). You may need to convert your frontmatter to YAML. Remove shortcodes to use standard Markdown files, or add Astro's optional MDX integration and replace shortcodes with component imports.

## Community Resources

- Add your own!