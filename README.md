# Astro Static Blog Site

This is an experimental Astro blog setup for learning how to build static sites with
GitHub-backed content.

## What is this project?

This is a **static blog site** built with Astro - a modern web framework that generates
fast, lightweight websites. Unlike dynamic sites that generate pages on-demand, static
sites pre-build all pages as HTML files that can be served quickly from any web server
or CDN.

## What we've set up

- **Astro framework** with TypeScript support for type safety
- **Blog template** with sample posts to explore
- **Local development environment** for experimentation
- **Content management** using Markdown/MDX files
- **Automatic optimization** for images, CSS, and JavaScript

## Understanding the tools

### npm (Node Package Manager)

- **What it is**: A tool for downloading and managing code libraries, plus running
  project tasks
- **Think of it like**: An app store + recipe book for your project
- **What we used it for**:
  - Downloaded the Astro blog template
  - Installed all necessary libraries (dependencies)
  - Set up development and build commands

## Available Commands

- `npm run dev` - Start development server at <http://localhost:4321/> (local only)
- `npm run dev -- --host` - Start dev server accessible on your local network
  (LAN/mobile testing)
- `npm run build` - Build the site for production (generates static HTML files)
- `npm run preview` - Preview the production build locally

### Previewing on your phone or other devices

To test your site on your phone or other devices on the same WiFi network:

1. Run the dev server with LAN access:

  ```sh
  npm run dev -- --host
  ```

1. Find your computer's local IP address (e.g., 192.168.1.42).
2. On your phone, open a browser and go to the address shown in the terminal
   (e.g., `http://192.168.1.42:4321` or similar).

This lets you preview changes instantly on your phone without pushing to Cloudflare.

## What's Included

- ✅ Minimal styling (make it your own!)
- ✅ 100/100 Lighthouse performance
- ✅ SEO-friendly with canonical URLs and OpenGraph data
- ✅ Sitemap support
- ✅ RSS Feed support
- ✅ Markdown & MDX support

## Key Files & Folders

- **`src/content/blog/`** - Your blog posts (Markdown/MDX files)
- **`src/pages/`** - Website pages (index, about, blog listings)
- **`src/components/`** - Reusable pieces of the site (header, footer, etc.)
- **`public/`** - Static files (images, fonts) that don't need processing
- **`package.json`** - Project configuration and dependencies list
- **`astro.config.mjs`** - Astro framework settings

## Getting Started with Content

1. **Edit existing posts**: Modify files in `src/content/blog/`
2. **Add new posts**: Create new `.md` or `.mdx` files in the blog folder
3. **Customize pages**: Edit files in `src/pages/` (like `about.astro`)
4. **Update site info**: Modify `src/consts.ts` for site title, description, etc.

## Authoring Content: .astro vs .md Files

You can create content for your site using either:

- **Markdown (`.md` or `.mdx`) files:**
  - Best for blog posts, articles, and long-form content.
  - Supports frontmatter for metadata (title, date, etc.).
  - Simple, readable, and easy to manage.
- **Astro (`.astro`) files:**
  - Best for custom pages, layouts, or when you need to mix content with
    components or logic.
  - Allows you to use Astro components, JavaScript/TypeScript, and advanced features.

Use Markdown for most content, and `.astro` files when you need more control or interactivity.

## Why Static Sites?

- **Fast loading**: Pre-built HTML loads instantly
- **Security**: No database or server-side code to hack
- **Reliable**: Works on any web server, including free hosting
- **SEO-friendly**: Search engines can easily crawl the content
- **GitHub integration**: Content can be managed through GitHub's interface

## 🚀 Project Structure

Your Astro project has this structure:

```text
├── public/              # Static files (images, fonts, favicon)
├── src/
│   ├── components/      # Reusable UI components
│   ├── content/         # Your blog posts and content
│   │   └── blog/        # Individual blog post files
│   ├── layouts/         # Page templates
│   ├── pages/           # Website pages (becomes URLs)
│   └── styles/          # CSS styling
├── astro.config.mjs     # Astro configuration
├── package.json         # Project dependencies and scripts
└── tsconfig.json        # TypeScript configuration
```

**How it works:**

- **Pages**: Files in `src/pages/` become website URLs (e.g., `about.astro` → `/about`)
- **Content**: Blog posts in `src/content/blog/` are managed as a collection
- **Components**: Reusable pieces like headers and footers in `src/components/`
- **Public**: Static files that don't need processing (images, fonts, etc.)

## Customization Quick Reference

Here are the key files to edit when customizing your site:

- **Edit the home page**: Modify content in `src/pages/index.astro`
- **Edit site header items**: Update navigation in `src/components/Header.astro`
- **Add your name to the footer**: Personalize `src/components/Footer.astro`
- **Check out included blog posts**: Browse `src/content/blog/` for examples
- **Customize blog post layout**: Modify `src/layouts/BlogPost.astro`

## Blog Post Properties

Blog posts in this project are authored as Markdown (`.md`) files and support
the following frontmatter properties:

- **`title`** (string, required): The title of the blog post.
- **`description`** (string, optional): A short description of the post.
- **`excerpt`** (string, optional): A longer excerpt or summary of the post.
- **`author`** (string, required): The name of the author.
- **`topic`** (string, optional): The topic or category of the post.
- **`pubDate`** (string, required): The publication date of the post (e.g., `Jan
  19 2018`).
- **`updatedDate`** (string, optional): The date the post was last updated.
- **`updatedExplanation`** (string, optional): A note explaining what was updated.
- **`heroImage`** (string, optional): The path to the hero image for the post.

These properties allow you to customize the metadata and appearance of each blog
post. To add a new post, create a Markdown file in the `src/content/blog/`
directory and include the desired frontmatter properties.

## Next Steps

1. **Visit your site**: The development server is running at <http://localhost:4321/>
2. **Explore the code**: Look at the sample blog posts in `src/content/blog/`
3. **Make changes**: Edit a blog post and see the site update automatically
4. **Add content**: Create new `.md` files for new blog posts
5. **Customize**: Modify the styling in `src/styles/global.css`

## Learning Resources

- [Astro Documentation](https://docs.astro.build) - Official Astro docs
- [Content Collections Guide](https://docs.astro.build/en/guides/content-collections/)
  - Managing blog content
- [Astro Discord](https://astro.build/chat) - Community support

## Project Repository and Workflow

This project is tracked in the GitHub repository:
[kompanek/drewkarnia-blog](https://github.com/kompanek/drewkarnia-blog)

- All source code, content, and configuration are version-controlled in this repo.
- Development is done locally, with changes committed and pushed to the `main`
  branch.
- Cloudflare Pages is connected to this repository and automatically builds and
  deploys the site on every push to `main`.
- To trigger a new deployment, simply push changes to GitHub:

  ```sh
  git add .
  git commit -m "Describe your change"
  git push
  ```

- The live site is updated automatically after each successful build.
- You can manage deployments and view build logs at the Cloudflare Pages dashboard:
  <https://dash.cloudflare.com>

## Deploying Dynamic Content with Cloudflare Workers

By default, this site is deployed as a static site using Cloudflare Pages. If you
want to add dynamic features (such as server-side rendering, API endpoints,
authentication, or edge logic), you can deploy your Astro site using Cloudflare
Workers.

### Why use Cloudflare Workers?

- **Server-side rendering (SSR):** Generate pages dynamically at request time.
- **APIs and edge logic:** Run custom JavaScript/TypeScript at the edge, close to
  your users.
- **Authentication, personalization, or A/B testing:** Handle requests
  dynamically based on user/session data.
- **Integrate with other services:** Fetch data from APIs or databases at
  runtime.

### How to deploy Astro with Cloudflare Workers

1. Install the Cloudflare adapter:

   ```sh
   npm install @astrojs/cloudflare
   ```

2. Update your `astro.config.mjs`:

   ```js
   import { defineConfig } from 'astro/config';
   import cloudflare from '@astrojs/cloudflare';

   export default defineConfig({
     output: 'server',
     adapter: cloudflare(),
   });
   ```

3. Add a `wrangler.toml` file to configure your Worker (see Cloudflare docs for
   details).
4. Set your build and deploy commands in Cloudflare:
   - Build command: `npm run build`
   - Deploy command: `npx wrangler deploy`

For more information, see the
[Astro Cloudflare adapter docs](https://docs.astro.build/en/guides/deploy/cloudflare/)
and [Cloudflare Workers documentation](https://developers.cloudflare.com/workers/).

## Working with Branches for Staging Changes

If you want to make major changes without publishing them immediately, use a
separate branch in your GitHub repository:

- Create a new branch for your changes:

  ```sh
  git checkout -b my-feature-branch
  ```

- Commit and push your changes to the branch as you work.
- The live site will only update when you merge your branch into `main` (or the
  branch configured for deployment in Cloudflare Pages).
- You can use pull requests to review and test changes before merging.

This workflow lets you stage, review, and test updates before they go live.

---

*This project was created using the Astro blog template and is ready for experimentation
with static site generation.*
