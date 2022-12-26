---
title: Migrating from SvelteKit
description: Tips for migrating an existing Sveltekit project to Astro
layout: ~/layouts/MigrationLayout.astro
stub: true
framework: Sveltekit
---

[SvelteKit](https://kit.svelte.dev) is a framework for building web applications on top of Svelte.

## Key Similarities between SvelteKit and Astro

SvelteKit and Astro share some similarities that will help you migrate your project:

- Both SvelteKit and Astro are modern Javascript static-site generators. Both use a `src/` folder for your project files and a special folder for file-based routing. Creating and managing pages for your site should feel familiar.

- Astro has [an official integration for using Svelte components](/en/guides/integrations-guide/svelte/) and support for NPM packages and community integrations, including several for Svelte. You will be able to write Svelte UI components for interactivity, and may be able to keep some or all of your existing components and dependencies.

- Astro and SvelteKit both allow you to use Headless CMSs, APIs or Markdown files for data. You can continue to use your preferred authoring system, and will be able to keep your existing content.

## Key Differences between SvelteKit and Astro

When you rebuild your SvelteKit site in Astro, you will notice some important differences:

- SvelteKit is a Svelte-based SPA (single-page application). Astro sites are multi-page apps built using `.astro` components, but can also support React, Preact, Vue.js, Svelte, SolidJS, AlpineJS, Lit and raw HTML templating.

- Astro was designed primarily for content-focused sites. An existing SvelteKit app might be built for high client-side interactivity and may include items that are difficult to replicate in Astro, such as dashboards.

- Astro includes built-in Markdown support, and includes a special frontmatter YAML `layout` property used per-file for page templating. If you are converting a Sveltekit Markdown-based blog, you will not have to install a separate Markdown integration and you will not set a layout via a configuration file. You can bring your existing Markdown files, but you may need to reorganize as Astro's file-based routing does not require a folder for each page route.


## Switch from SvelteKit to Astro

To convert a SvelteKit blog to Astro, start with our blog theme starter template, or explore more community blog themes in our [theme showcase](https://astro.build/themes). Bring your existing Markdown (or MDX, with our optional integration) files as content to [create Markdown or MDX pages](/en/guides/markdown-content/).

While file-based routing and layout components are similar in Astro, you may wish to read about [Astro's project structure](/en/core-concepts/project-structure/) to learn where files should be located.

To convert other types of sites, such as a portfolio or documentation site, see more official starter templates on [astro.new](https://astro.new) with links to a GitHub repository as well as one-click links to open a working project in StackBlitz, CodeSandbox and Gitpod online development environments.

## Community Resources

- Blog Post: [Rewriting my blog from SvelteKit to Astro](https://kharann.com/blog/rewriting-my-blog/)

- Add your own!