# Scientific AI Lab (SAIL) Website

This repository contains the source code for the SAIL website, built with React, Vite, and Markdown.

## How to Update Content
All textual content and data are stored as Markdown files. To update the website, edit the files located in the `public/content/` directory:
- `public/content/about.md`: Profile and Lab Members
- `public/content/research.md`: Research Topics
- `public/content/publications.md`: Publications List
- `public/content/all_posts.md`: News and Announcements

**Note:** Do not edit the files in the `dist` folder directly, as they are overwritten during the build process.

## Local Development
To preview your changes locally before deploying:
```bash
# Start the local development server
npm run dev
```

## How to Deploy to GitHub Pages
Whenever you make changes to the code or markdown files, follow these exact steps to publish them to the live website:

**1. Build the project**
Converts your React code and markdown into optimized HTML/CSS/JS in the `dist` folder.
```bash
npm run build
```

**2. Commit your changes to the main branch**
Saves your source code changes.
```bash
git add .
git commit -m "Update: [Brief description of what you changed]"
git push origin main
```

**3. Deploy to GitHub Pages**
Pushes only the built `dist` folder to the `gh-pages` branch, updating the live site.
```bash
git subtree push --prefix dist origin gh-pages
```

### Deployment Shortcut (All-in-One Command)
You can copy and paste this single line to do all three steps at once:
```bash
npm run build && git add . && git commit -m "Update content" && git push origin main && git subtree push --prefix dist origin gh-pages
```
