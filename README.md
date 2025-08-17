# Astro Static Blog Site

This is an experimental Astro blog setup for learning how to build static sites with GitHub-backed content.

## What is this project?

This is a **static blog site** built with Astro - a modern web framework that generates fast, lightweight websites. Unlike dynamic sites that generate pages on-demand, static sites pre-build all pages as HTML files that can be served quickly from any web server or CDN.

## What we've set up

- **Astro framework** with TypeScript support for type safety
- **Blog template** with sample posts to explore
- **Local development environment** for experimentation
- **Content management** using Markdown/MDX files
- **Automatic optimization** for images, CSS, and JavaScript

## Understanding the tools

### npm (Node Package Manager)

- **What it is**: A tool for downloading and managing code libraries, plus running project tasks
- **Think of it like**: An app store + recipe book for your project
- **What we used it for**:
  - Downloaded the Astro blog template
  - Installed all necessary libraries (dependencies)
  - Set up development and build commands

## Available Commands

- `npm run dev` - Start development server at <http://localhost:4321/>
- `npm run build` - Build the site for production (generates static HTML files)
- `npm run preview` - Preview the production build locally

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

## Next Steps

1. **Visit your site**: The development server is running at <http://localhost:4321/>
2. **Explore the code**: Look at the sample blog posts in `src/content/blog/`
3. **Make changes**: Edit a blog post and see the site update automatically
4. **Add content**: Create new `.md` files for new blog posts
5. **Customize**: Modify the styling in `src/styles/global.css`

## Learning Resources

- [Astro Documentation](https://docs.astro.build) - Official Astro docs
- [Content Collections Guide](https://docs.astro.build/en/guides/content-collections/) - Managing blog content
- [Astro Discord](https://astro.build/chat) - Community support

---

*This project was created using the Astro blog template and is ready for experimentation with static site generation.*
