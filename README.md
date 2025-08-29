# Teaching Website (GitHub Pages + Minimal Mistakes)

## Quick Start (GitHub Desktop)
1. **Create a new GitHub repository** (public) named, for example, `teaching-site`.
2. **Download** the ZIP from ChatGPT and **extract** it.
3. In **GitHub Desktop**: *File → Add local repository…* and point to the extracted folder. Commit & **Publish** to GitHub.
4. On GitHub: *Settings → Pages*. Set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` (root)
   - Save. Wait for the site to build.
5. Your site will be at `https://<your-username>.github.io/<repo-name>/` (copy this into `_config.yml` `url` later).

## Customize
- Edit `_config.yml` (title, author links, etc.).
- Add lecture videos in **Lectures** using `{% include video id="VIDEO_ID" provider="youtube" %}`.
- Put PDFs in `assets/pdfs/` and link to them from **Materials**.
- Replace `assets/img/header.jpg` and `assets/img/avatar.jpg` with your images.
- Blog posts go into `_posts/` as `YYYY-MM-DD-title.md`.

## Tips
- Keep filenames URL-friendly (lowercase, dashes).
- To organize courses by year, add new sections in **Lectures** and **Materials**.
- If you prefer a custom domain: add a `CNAME` file with your domain and point DNS to GitHub Pages.

## Local Preview (optional, requires Ruby)
```bash
bundle install
bundle exec jekyll serve
```
Then open http://localhost:4000
